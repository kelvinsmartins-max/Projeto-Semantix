<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Projeto de Parceria Semantix - Raio-X do Funcionalismo Federal</title>
    <style>
        @media print {
            @page {
                size: A4;
                margin: 20mm 15mm 20mm 15mm;
            }
            body {
                background-color: #ffffff;
            }
        }
        
        * {
            box-sizing: border-box;
        }

        body {
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            color: #2d3748;
            line-height: 1.6;
            font-size: 10.5pt;
            margin: 0;
            padding: 0;
            background-color: #f7fafc;
        }

        .container {
            max-width: 800px;
            margin: 40px auto;
            background: #ffffff;
            padding: 40px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            border-radius: 8px;
        }

        /* --- CAPA --- */
        .cover {
            background-color: #1a365d;
            padding: 60px 40px;
            color: #ffffff;
            border-radius: 6px;
            margin-bottom: 40px;
        }

        .cover-header {
            font-size: 12pt;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: #63b3ed;
            margin-bottom: 20px;
            font-weight: bold;
        }

        .cover-title {
            font-size: 28pt;
            font-weight: 800;
            line-height: 1.2;
            color: #ffffff;
            margin-bottom: 15px;
        }

        .cover-subtitle {
            font-size: 14pt;
            color: #cbd5e0;
            margin-bottom: 60px;
            font-weight: 300;
        }

        .cover-footer {
            border-top: 1px solid #4a5568;
            padding-top: 20px;
            font-size: 10pt;
            color: #cbd5e0;
            display: flex;
            justify-content: space-between;
        }

        /* --- CONTEÚDO --- */
        .section {
            margin-bottom: 40px;
            page-break-before: always;
        }

        h1 {
            font-size: 20pt;
            color: #1a365d;
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 8px;
            margin-top: 0;
            margin-bottom: 20px;
        }

        h2 {
            font-size: 14pt;
            color: #2b6cb0;
            margin-top: 25px;
            margin-bottom: 12px;
            border-left: 4px solid #3182ce;
            padding-left: 10px;
        }

        p {
            margin-bottom: 15px;
            text-align: justify;
        }

        ul, ol {
            margin-bottom: 20px;
            padding-left: 20px;
        }

        li {
            margin-bottom: 8px;
        }

        .highlight-box {
            background-color: #ebf8ff;
            border-left: 4px solid #3182ce;
            padding: 15px;
            margin: 20px 0;
            border-radius: 4px;
        }

        .math {
            font-family: 'Times New Roman', Times, serif;
            font-style: italic;
            font-weight: bold;
            color: #2c5282;
        }

        code {
            font-family: 'Courier New', Courier, monospace;
            background-color: #edf2f7;
            padding: 2px 6px;
            border-radius: 4px;
            font-size: 9.5pt;
        }

        .dashboard-btn-container {
            text-align: center;
            margin: 30px 0;
        }

        .dashboard-link {
            color: #ffffff !important;
            background-color: #2b6cb0;
            border: 1px solid #2b6cb0;
            padding: 14px 24px;
            display: inline-block;
            border-radius: 6px;
            text-decoration: none;
            font-weight: bold;
            font-size: 11pt;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .dashboard-link:hover {
            background-color: #2c5282;
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- CAPA -->
        <div class="cover">
            <div class="cover-header">Projeto de Parceria | Semantix</div>
            <div class="cover-title">Raio-X do<br>Funcionalismo Federal</div>
            <div class="cover-subtitle">Uma análise analítica e visual sobre a alocação de pessoal e impacto fiscal do passivo de aposentados e pensionistas</div>
            
            <div class="cover-footer">
                <div>
                    <strong>Autor:</strong> Kelvin Martins<br>
                </div>
            </div>
        </div>

        <!-- PÁGINA 1: INTRODUÇÃO E COLETA -->
        <div class="section">
            <h1>1. Introdução e Coleta de Dados</h1>
            <p>
                O gerenciamento de recursos humanos no setor público brasileiro é uma atividade crítica sob a ótica fiscal. 
                A dinâmica entre a contratação de novos servidores públicos e a acumulação histórica de aposentadorias (inativos) 
                e pensões dita o ritmo das contas do Governo Federal. Este documento apresenta o relatório técnico de entrega do 
                projeto desenvolvido no escopo da parceria acadêmica/corporativa com a <strong>Semantix</strong>.
            </p>

            <h2>1.1. Formulação do Problema</h2>
            <p>
                A ausência de visualizações consolidadas sobre o funcionalismo federal dificulta a identificação rápida de gargalos 
                operacionais e desafios previdenciários. Diante disso, este projeto visa responder a três questões centrais:
            </p>
            <ul>
                <li>Quais Órgãos Superiores concentram as maiores parcelas de força ativa e passiva do governo?</li>
                <li>Qual é a proporção real entre servidores ativos e o passivo previdenciário (inativos/pensionistas)?</li>
                <li>Existe uma correlação estatística direta e modelável entre o volume de ativos e o de inativos em nível institucional?</li>
            </ul>

            <h2>1.2. Origem das Fontes de Dados</h2>
            <p>
                Para dar suporte à análise, as bases oficiais foram extraídas do <strong>Portal da Transparência</strong> e do 
                <strong>Painel Estatístico de Pessoal (PEP)</strong>, ambos de responsabilidade do Ministério da Gestão e da Inovação 
                em Serviços Públicos (MGI). 
            </p>
            <p>
                O conjunto de dados final consolidado abrange <strong>326 linhas</strong> (registros), representando as divisões 
                institucionais do Governo Federal por meio de suas respectivas pastas e autarquias (Órgãos de Lotação).
            </p>

            <div class="highlight-box">
                <strong>Métricas Estruturadas Coletadas:</strong>
                <ul>
                    <li><code>Servidores</code>: Volume total de servidores ativos de cada órgão.</li>
                    <li><code>Inativos</code>: Total de aposentados vinculados à pasta.</li>
                    <li><code>Pensionistas</code>: Beneficiários de pensões instituídas por servidores falecidos.</li>
                </ul>
            </div>
        </div>

        <!-- PÁGINA 2: MODELAGEM -->
        <div class="section">
            <h1>2. Modelagem e Preparação dos Dados</h1>
            <p>
                O processo de modelagem de dados foi estruturado inteiramente na linguagem <strong>Python</strong> utilizando a biblioteca 
                <strong>Pandas</strong> para higienização e tratamento (ETL), e visualizações analíticas integradas via 
                <strong>Matplotlib</strong> e <strong>Seaborn</strong>.
            </p>

            <h2>2.1. Higienização e Pipeline de Tratamento (ETL)</h2>
            <p>
                O arquivo CSV original possuía inconsistências comuns causadas por exportações do Windows Excel, as quais foram sanadas 
                sistematicamente através dos seguintes passos operacionais:
            </p>
            <ol>
                <li><strong>Mapeamento de Delimitadores:</strong> Correção do separador de campos para ponto e vírgula (<code>;</code>) e codificação ocidental (<code>utf-8</code> / <code>latin1</code>) para evitar falhas de leitura.</li>
                <li><strong>Limpeza de Strings e Colunas Nulas:</strong> Eliminação de aspas adicionais nas colunas, remoção de caracteres de formatação invisíveis gerados por erros de encoding e exclusão da coluna vazia <code>Unnamed: 5</code>.</li>
                <li><strong>Agrupamento e Agregação:</strong> Consolidação de dados a nível de Órgão Superior de Lotação para possibilitar comparações de macro-impacto (como o total concentrado nos Ministérios da Educação e Defesa).</li>
            </ol>

            <h2>2.2. Modelagem Matemática (Análise de Correlação)</h2>
            <p>
                Para quantificar matematicamente a dinâmica entre a força ativa e inativa do Estado, o modelo utilizou a formulação de 
                correlação linear de Pearson. O algoritmo foi executado nativamente sobre as variáveis numéricas correspondentes de cada órgão:
            </p>
            
            <div style="text-align:center; margin:15px 0; font-size:1.15em;">
                <span class="math">r = &Sigma; (x<sub>i</sub> − x̅)(y<sub>i</sub> − y̅) / &radic;&Sigma; (x<sub>i</sub> − x̅)<sup>2</sup> &Sigma; (y<sub>i</sub> − y̅)<sup>2</sup></span>
            </div>

            <p>
                Onde <span class="math">x</span> representa o contingente de servidores ativos e <span class="math">y</span> representa o volume de aposentados (inativos). 
                O cálculo resultou em uma taxa de correlação linear extremamente acentuada, descrita na seção de conclusões.
            </p>
        </div>

        <!-- PÁGINA 3: CONCLUSÕES -->
        <div class="section">
            <h1>3. Conclusões e Insights Analíticos</h1>
            <p>
                Após a execução do pipeline de dados em Python e a criação do dashboard interativo no <strong>Looker Studio</strong>, 
                foi possível extrair conclusões de alta relevância estratégica para a governança do funcionalismo federal:
            </p>

            <h2>3.1. Distribuição Simétrica da Folha (O Desafio Previdenciário)</h2>
            <p>
                A análise proporcional do banco de dados agregados revelou que apenas <strong>48%</strong> de toda a estrutura do funcionalismo 
                analisada é composta por servidores ativos (em atividade). A outra fatia — correspondente a <strong>52%</strong> — é dividida 
                entre aposentados (<strong>27,7%</strong>) e pensionistas (<strong>24,3%</strong>). 
            </p>

            <h2>3.2. Concentração Crítica nos Ministérios Líderes</h2>
            <p>
                Os dados indicam que o <strong>Ministério da Educação (MEC)</strong> e o <strong>Ministério da Defesa</strong> dominam com 
                larga vantagem o volume de vínculos no Executivo Federal. O MEC apresenta um modelo de equilíbrio entre servidores ativos de 
                universidades e seu respectivo histórico de aposentadorias, enquanto a Defesa destaca-se pela elevadíssima quantidade de 
                pensionistas.
            </p>

            <h2>3.3. Validação do Coeficiente Estatístico</h2>
            <p>
                O cálculo da correlação de Pearson gerou um coeficiente de:
            </p>
            <div class="highlight-box" style="text-align: center; font-size: 11pt; background-color: #f0fff4; border-left-color: #38a169; color: #276749; margin: 10px 0;">
                <strong>Coeficiente de Correlação de Pearson: <span class="math">r = 0,91</span> (Muito Forte)</strong>
            </div>

            <h2>3.4. Dashboard Interativo no Looker Studio</h2>
            <p>
                Como produto visual de ponta a ponta, foi estruturado um painel interativo de inteligência que consome a base de dados tratada de 326 registros. O dashboard oferece visualizações focadas no perfil de distribuição de funcionários por órgão superior e análise de proporção de vínculos históricos. Ele pode ser acessado diretamente através do link seguro abaixo:
            </p>
            
            <div class="dashboard-btn-container">
                <a class="dashboard-link" href="https://datastudio.google.com/reporting/73942657-76fd-41f4-9880-4361a54c1269" target="_blank">
                    🔗 Acessar o Dashboard no Looker Studio
                </a>
            </div>

            <h2>3.5. Sugestões de Ações Estratégicas</h2>
            <ul>
                <li><strong>Modernização e Transição Digital:</strong> Direcionamento de investimentos de automatização e Inteligência Artificial prioritariamente no MEC e na Defesa devido ao ganho de escala que esses órgãos proporcionam.</li>
                <li><strong>Planejamento de Força de Trabalho (PFT):</strong> Substituição da reposição automática de servidores aposentados por reestruturações de carreira com base em eficiência digital.</li>
            </ul>
        </div>
    </div>

</body>
</html>