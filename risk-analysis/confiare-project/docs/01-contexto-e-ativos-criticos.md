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

### Ativo 2: PostgreSQL 16 (Banco de Dados)

É onde ficam armazenados todos os dados dos clientes: cadastros, apólices, sinistros e informações financeiras.

| Dimensão | Nível | Por quê? |
|---|---|---|
| Confidencialidade | Alta | Contém dados sensíveis de clientes (CPF, dados de saúde, informações bancárias) protegidos pela LGPD. Um vazamento gera multas e perda de confiança. |
| Integridade | Alta | Se os dados de uma apólice ou sinistro forem alterados indevidamente, a empresa pode pagar valores errados ou negar coberturas devidas. |
| Disponibilidade | Alta | Sem acesso ao banco, nenhum sistema funciona: não dá para consultar apólices, registrar sinistros ou emitir documentos. |

### Ativo 3: Fortinet FortiGate 100F (Dispositivo de Rede)

É o firewall responsável por proteger a rede da Confiare, filtrando o tráfego entre a internet e os sistemas internos.

| Dimensão | Nível | Por quê? |
|---|---|---|
| Confidencialidade | Média | Configurações de rede e regras de segurança podem revelar a estrutura interna da empresa a um invasor, facilitando outros ataques. |
| Integridade | Alta | Se as regras do firewall forem alteradas indevidamente, um invasor pode abrir brechas de acesso não autorizado à rede. |
| Disponibilidade | Alta | Se o firewall falhar ou for desligado, a rede fica exposta ou totalmente inacessível, interrompendo a operação. |

### Ativo 4: macOS Sonoma 14.x (Estações de Trabalho)

Sistema operacional usado nos computadores dos colaboradores para acessar sistemas internos, e-mails e documentos.

| Dimensão | Nível | Por quê? |
|---|---|---|
| Confidencialidade | Média | Estações armazenam ou acessam temporariamente dados de clientes e documentos internos, que podem ser expostos em caso de invasão do dispositivo. |
| Integridade | Média | Um dispositivo comprometido pode ser usado para alterar documentos ou enviar informações falsas em nome do colaborador. |
| Disponibilidade | Média | A indisponibilidade afeta a produtividade individual do colaborador, mas não interrompe a operação como um todo. |

### Ativo 5: Safari (Navegador de Internet)

Principal navegador utilizado pelos colaboradores para acessar sistemas internos web e serviços externos.

| Dimensão | Nível | Por quê? |
|---|---|---|
| Confidencialidade | Média | Senhas salvas, cookies de sessão e histórico podem expor credenciais de acesso a sistemas internos se o navegador for comprometido. |
| Integridade | Baixa | Riscos de integridade são limitados, já que o navegador não armazena dados críticos por conta própria. |
| Disponibilidade | Baixa | A indisponibilidade do navegador tem impacto pontual e facilmente contornável (uso de outro navegador). |
