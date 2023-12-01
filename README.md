Pipeline de Segurança
Visão Geral
Este repositório utiliza uma pipeline de segurança para garantir a qualidade e a segurança do código fonte. As ferramentas escolhidas ajudam a identificar vulnerabilidades, aplicar boas práticas de codificação e realizar testes de segurança automatizados.

Ferramentas de Segurança
1. Snyk
Snyk é uma ferramenta de segurança que analisa dependências do projeto em busca de vulnerabilidades conhecidas. É integrada à pipeline para identificar e corrigir potenciais brechas de segurança.

Como funciona:

A cada push ou pull request, a pipeline executa verificações de segurança usando o Snyk.
As vulnerabilidades são apresentadas no painel do Snyk e, se necessário, são automaticamente corrigidas usando o comando snyk wizard.
Configuração:

É necessário configurar as variáveis de ambiente, incluindo o token do Snyk, no ambiente de execução da pipeline.
2. OWASP ZAP (Dynamic Application Security Testing - DAST)
OWASP Zed Attack Proxy (ZAP) é utilizado para testes de segurança dinâmica, analisando a aplicação enquanto ela está em execução.

Como funciona:

Durante a pipeline, uma imagem Docker é construída e executada para a aplicação.
O ZAP realiza varreduras de segurança na aplicação para identificar potenciais vulnerabilidades.
O relatório de segurança é gerado e armazenado como um artefato.
Configuração:

A configuração envolve a construção da imagem Docker da aplicação e a execução do ZAP com parâmetros específicos.
Executando a Pipeline Localmente
Instalação de Dependências:

Certifique-se de ter o Docker instalado localmente.
Instale as dependências do Python usando pip install -r requirements.txt.
Configuração de Variáveis de Ambiente:

Crie um arquivo .env na raiz do projeto com as variáveis de ambiente necessárias.
Execução:

Execute a pipeline localmente usando o seguinte comando:
bash
Copy code
./run_pipeline.sh
Resultados:

Os resultados das verificações de segurança, incluindo relatórios do Snyk e ZAP, estarão disponíveis localmente.
Contribuições
Contribuições são bem-vindas! Se você identificar melhorias ou tiver sugestões para aprimorar a segurança da pipeline, sinta-se à vontade para abrir issues ou pull requests.

