Pipeline de Segurança
Visão Geral
Este repositório implementa uma robusta pipeline de segurança para assegurar a qualidade e a segurança do código-fonte. As ferramentas escolhidas são fundamentais para identificar vulnerabilidades, aplicar boas práticas de codificação e conduzir testes de segurança automatizados.

Ferramentas de Segurança
1. Snyk
Snyk é uma ferramenta de segurança especializada na análise de dependências de projetos em busca de vulnerabilidades conhecidas. Integrada à pipeline, ela identifica e, quando possível, corrige potenciais brechas de segurança.

Como Funciona:
A cada push ou pull request, a pipeline realiza verificações de segurança usando o Snyk.
As vulnerabilidades são apresentadas no painel do Snyk, proporcionando uma visão clara do estado da segurança.

![image](https://github.com/kennedycAlves/flask-restplus-server-example/assets/41455653/682ef4be-63f9-471b-a5a0-216de420a665)



2. OWASP ZAP (Dynamic Application Security Testing - DAST) (Não está funcionando por conta de problemas na imagem Docker)
OWASP Zed Attack Proxy (ZAP) é utilizado para testes de segurança dinâmica, analisando a aplicação enquanto está em execução.

Como Funciona:
Durante a pipeline, uma imagem Docker é construída e executada para a aplicação.
O ZAP conduz varreduras de segurança na aplicação, identificando potenciais vulnerabilidades.
Relatórios de segurança são gerados e armazenados como artefatos valiosos.

path: .github/workflows


