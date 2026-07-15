# Raio-X do Funcionalismo Federal: Para onde vão os recursos de pessoal?
> **Projeto de Parceria | Semantix**  
> **Autor:** Kelvin Martins  
> **Data:** Julho de 2026  
> **Status:** Finalizado (Entregável do Checklist de Projeto)

---

## 📖 Apresentação do Projeto
Este repositório contém a entrega oficial do projeto de análise de dados desenvolvido em parceria com a **Semantix**. O objetivo principal é mapear a alocação de força de trabalho do Governo Federal do Brasil (servidores ativos, aposentados e pensionistas) para compreender o impacto previdenciário e apontar caminhos para a transformação digital em áreas-chave.

---

## 1. Coleta de Dados

### 1.1. Formulação do Problema e Justificativa
O monitoramento e a governança fiscal do pessoal público federal são complexos devido à descentralização de informações. Este projeto buscou diagnosticar a distribuição real entre a atividade operacional do Estado (servidores ativos) e o passivo financeiro acumulado (aposentados e pensionistas) para responder:
* Onde estão concentrados os maiores volumes de servidores?
* Qual a proporção de gastos ativos vs. inativos?
* Existe dependência linear estatística direta no crescimento do contingente previdenciário por órgão?

### 1.2. Origem e Estrutura dos Dados
* **Fonte Oficial:** Portal da Transparência / Painel Estatístico de Pessoal (PEP) do Ministério da Gestão e da Inovação em Serviços Públicos (MGI).
* **Volume:** Consolidação de **326 registros (linhas)** agregados por órgãos e autarquias públicas.
* **Variáveis Tratadas:**
  * `Órgão Superior Lotação`: O ministério controlador.
  * `Órgão Lotação`: A autarquia ou órgão específico de trabalho.
  * `Servidores`: Quantidade de servidores ativos.
  * `Inativos`: Quantidade de aposentados públicos.
  * `Pensionistas`: Quantidade de pensionistas registrados.

---

## 2. Modelagem e Preparação dos Dados

A preparação e a análise exploratória de dados (AED) foram conduzidas inteiramente em **Python** (via Jupyter Notebook). 

### 2.1. Higienização e Pipeline de Tratamento (ETL)
O arquivo bruto de dados apresentava caracteres corrompidos originados pelo encoding do Windows Excel e colunas vazias. O pipeline de tratamento corrigiu esses fatores:
1. **Configuração do Carregador:** Forçamento do separador de campos para ponto e vírgula (`;`) para evitar quebra no processo de parse.
2. **Data Cleaning:** Limpeza de aspas remanescentes nas colunas e remoção automática de colunas nulas (`Unnamed: 5`).
3. **Agregação Estratégica:** Consolidação e agrupamento a nível de Órgão Superior para permitir análises transversais de liderança fiscal.

### 2.2. Modelagem Estatística (Correlação de Pearson)
Para quantificar a dependência entre a força de trabalho ativa e o passivo previdenciário subsequente de cada órgão, o modelo aplicou o Coeficiente de Correlação de Pearson de forma nativa na base agregada:

$$r = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum (x_i - \bar{x})^2 \sum (y_i - \bar{y})^2}}$$

Onde:
* $x$ = Número de servidores ativos em um órgão.
* $y$ = Número de aposentados (inativos).

O código Python contendo este fluxo está disponível neste repositório sob o nome `analise_fopag.ipynb`.

---

## 3. Conclusões e Insights do Projeto

A partir do processamento dos dados e da criação do painel no Looker Studio, as seguintes conclusões estratégicas foram consolidadas:

### 3.1. Proporção Crítica da Folha
* **Ativos (Servidores):** Representam apenas **48%** da força mapeada.
* **Inativos e Pensionistas:** Compõem **52%** do total de vínculos da base (sendo 27,7% aposentados e 24,3% pensionistas).
* **Conclusão:** Há um enorme desafio fiscal previdenciário no Brasil, onde o custo de manutenção da folha de inativos supera o volume de profissionais que mantém a máquina ativa.

### 3.2. Dominância dos Ministérios Líderes
O Ministério da Educação (MEC) e o Ministério da Defesa concentram, de forma disparada, o maior contingente total de vínculos do funcionalismo. 
* A Educação lidera com o maior equilíbrio de ativos e inativos de suas autarquias e universidades.
* A Defesa destaca-se pela proporção massiva de pensionistas gerados historicamente.

### 3.3. Validação do Coeficiente de Correlação
* **Resultado:** $r = 0.91$
* **Significância:** Uma correlação linear de **0,91** é classificada como **Muito Forte**. Isso valida empiricamente que a ampliação imediata de contratações de servidores ativos por órgão gera um impacto previdenciário futuro direto e previsível na exata proporção da força de trabalho inicial.

### 3.4. Sugestões de Ações baseadas nos Resultados
* **Aposta Tecnológica Focada:** Projetos de automação de processos de negócios e inteligência de dados devem priorizar o MEC e a Defesa por sua alta escala corporativa de impacto.
* **Planejamento de Força de Trabalho (PFT):** O governo deve vetar a contratação reativa padrão (reposição 1 para 1) e adotar políticas que priorizem a digitalização de serviços e a reestruturação de carreiras antes de abrir novos processos de seleção.

---

## 📊 Dashboard Interativo
O painel de visualização completo e interativo foi construído no Looker Studio e pode ser consultado no link abaixo:
* **[Link de Acesso ao Painel do Looker Studio]** *(Substitua por seu link público do Looker Studio)*
