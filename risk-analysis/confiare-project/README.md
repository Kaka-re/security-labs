# Análise e Gestão de Riscos de Segurança da Informação 
# Confiare

Consultoria de segurança da informação para a Confiare, uma seguradora fictícia usada como estudo de caso, cobrindo identificação de ativos críticos, análise de riscos, plano de tratamento e um processo de gestão de vulnerabilidades.

## Escopo do trabalho

- Identificação e classificação de ativos críticos pelo modelo CID (Confidencialidade, Integridade, Disponibilidade)
- Análise de 27 riscos, organizados em quatro frentes:
  - Riscos OWASP (falhas em sistemas web)
  - Ameaças gerais e operacionais
  - Riscos de segurança da informação
  - Riscos de privacidade (LGPD)
- Plano de tratamento por risco, com ações Preventivas, Detectivas e Corretivas
- Proposta de processo formal de gestão de vulnerabilidades, com monitoramento contínuo via NIST NVD
- 
##  Metodologias e referências

- Modelo CID (Confidencialidade, Integridade, Disponibilidade)
- OWASP Top 10 / OWASP Risk Rating Methodology
- Lei Geral de Proteção de Dados (Lei nº 13.709/2018) e Resolução CD/ANPD nº 2/2022
- NIST National Vulnerability Database (NVD)

## Estrutura do repositório

| Pasta/Arquivo | Conteúdo |
|---|---|
| `README.md` | Visão geral do projeto |
| `docs/01-contexto-e-ativos-criticos.md` | Ativos e classificação CID |
| `docs/02-analise-detalhada-de-riscos.md` | Os 27 riscos identificados |
| `docs/03-plano-de-tratamento-dos-riscos.md` | Ações preventivas, detectivas e corretivas |
| `docs/04-gestao-de-vulnerabilidades.md` | Processo de gestão + gráficos |
| `data/relatorio_vulnerabilidades.xlsx` | Série histórica de vulnerabilidades |
| `assets/` | Imagens/gráficos usados na documentação |

## 📊 Destaques dos Dados

Ao longo do período monitorado (mar/2026 a mai/2026), foram identificados 193 registros de vulnerabilidades nos ativos críticos, com a seguinte distribuição por severidade:

| Severidade | Total |
|---|---|
| CRITICAL | 2 |
| HIGH | 57 |
| MEDIUM | 112 |
| LOW | 12 |
| N/A | 10 |

Detalhamento completo por ativo e por quinzena disponível em [`data/relatorio_vulnerabilidades.xlsx`](data/relatorio_vulnerabilidades.xlsx) e nos gráficos em [`docs/04-gestao-de-vulnerabilidades.md`](docs/04-gestao-de-vulnerabilidades.md).

##  Ativos críticos mapeados

| Ativo | Tipo |
|---|---|
| Ubuntu Server | Sistema Operacional (Servidor) |
| PostgreSQL 16 | Banco de Dados |
| Fortinet FortiGate 100F | Dispositivo de Rede |
| macOS Sonoma 14.x | Estações de Trabalho |
| Safari | Navegador de Internet |

Detalhes da classificação CID de cada ativo em [`docs/01-contexto-e-ativos-criticos.md`](docs/01-contexto-e-ativos-criticos.md).


