# Relatório de Contexto e Ativos Críticos

## Introdução

Este relatório foi elaborado pela Confiare, uma seguradora brasileira, com o objetivo de identificar os principais sistemas e informações da empresa (chamados de ativos), classificar o quanto cada um precisa ser protegido e, posteriormente, levantar os principais riscos e como tratá-los.

Usamos como base o modelo CID, que avalia três aspectos de cada ativo:

- **Confidencialidade (C):** as informações podem ser vistas só por quem tem permissão?
- **Integridade (I):** as informações estão corretas e não foram alteradas indevidamente?
- **Disponibilidade (D):** o sistema está funcionando quando as pessoas precisam dele?

Em conformidade com as boas práticas e a Lei Geral de Proteção de Dados (Lei nº 13.709/2018).

## Quem é a Confiare

A Confiare é uma seguradora que opera no setor de seguros. No dia a dia, ela lida com dados muito sensíveis dos seus clientes como CPF, informações de saúde, dados bancários, entre outros.

Seu perfil tecnológico é composto por: servidor Linux (Ubuntu Server), banco de dados relacional PostgreSQL 16, dispositivo de segurança de rede Fortinet FortiGate 100F e estações de trabalho Apple MacBook com macOS Sonoma 14.x. O principal navegador utilizado pelos colaboradores é o Safari.

## Identificação e Classificação CID dos Ativos Críticos

A seguir, avaliamos cada sistema da Confiare como Alta, Média ou Baixa em cada dimensão do CID, explicando o motivo com exemplificações.

### Ativo 1: Ubuntu Server (Sistema Operacional do Servidor)

Todos os sistemas rodam nele: o portal de apólices, o banco de dados e as integrações com parceiros. É o núcleo operacional de toda a infraestrutura.

| Dimensão | Nível | Por quê? |
|---|---|---|
| Confidencialidade | Alta | Se alguém invadir o servidor, consegue ver tudo: CPF, laudos médicos e dados bancários dos clientes. Isso viola a LGPD. |
| Integridade | Alta | Arquivos importantes ficam no servidor. Se alguém alterar esses arquivos, a empresa pode cobrar valores errados e ter prejuízo financeiro. |
| Disponibilidade | Alta | Se o servidor cair, a empresa para completamente: não consegue emitir apólices, consultar sinistros nem atender clientes. |
