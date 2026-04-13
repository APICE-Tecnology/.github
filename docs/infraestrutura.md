![Documentação TI](https://utils.storage.apicesaudemental.link/documentacao-ti.png)

# Infraestrutura e Sistemas — apice

Mapa completo dos sistemas, domínios, serviços e integrações em operação.

---

## Domínios

| Domínio | Status | Propósito |
|---|---|---|
| [clinicaapice.com.br](https://clinicaapice.com.br) | configurando | Site institucional principal |
| [apicesaudemental.link](https://apicesaudemental.link) | ativo | Domínio base dos sistemas digitais internos |
| [institutoapice.org.br](https://institutoapice.org.br) | ativo | Site e plataforma do Instituto APICE |
| [institutoapice.com.br](https://institutoapice.com.br) | ativo | Domínio alternativo do Instituto |
| [apicegrupo.com.br](https://apicegrupo.com.br) | configurando | Site corporativo do grupo |

---

## Plataformas digitais

Todas as plataformas digitais são hospedadas no **Cloudflare Pages** e servidas via CDN global.

---

## Backends e APIs

Os serviços de backend rodam como **Cloudflare Workers** — serverless, executados na borda da rede.

---

## Armazenamento — Cloudflare R2

Armazenamento de objetos (arquivos, assets, relatórios e vídeos).

---

## Banco de dados

| Serviço | Localização | Uso |
|---|---|---|
| **Supabase (PostgreSQL)** | Cloud |
| **SQL Server** | Local (rede interna) |
| **Redis** | Local | Cache e filas de processamento assíncrono |
| **Cloudflare Hyperdrive** | Edge | Pool de conexões entre Workers e Supabase |

---

## Sistema clínico — Smart Pixeon

O prontuário eletrônico, agenda de consultas e gestão clínica são gerenciados pelo **Smart**, sistema ERP/PEP da [Pixeon](https://www.pixeon.com/).

- Opera na **rede local** das unidades (não depende de internet)
- Acesso via estações internas ou VPN
- Dados de pacientes, evoluções, prescrições e agenda centralizada

### Integrações do Smart

| Parceiro | Integração |
|---|---|
| [Wellon](https://wellon.digital/) | Plataforma de saúde digital — conectada ao Smart para fluxos assistenciais |
| [Zerodox](https://www.zerodox.com.br/) | Gestão e operações de saúde integradas ao sistema |

---

## Painéis e totems

Os painéis de chamada de pacientes e totems de autoatendimento nas unidades são operados por scripts locais (.bat) que injetam sessões no Smart via cookies.

**Repositório:** [APICE-Tecnology/PAINEL-TOTEM](https://github.com/APICE-Tecnology/PAINEL-TOTEM)

Cada painel e totem tem um `cookies.json` com configuração de setor, fila e locais de chamada.
A comunicação ocorre via rede local com o servidor Smart.

---

## Centro de chamados

O gerenciamento de tarefas, chamados de TI e projetos internos é feito via **ClickUp**.

| Item | Detalhe |
|---|---|
| Plataforma | [ClickUp](https://clickup.com/) |
| Uso | Chamados de TI, gestão de projetos, documentação de tarefas |
| Acesso | Equipe interna — solicite ao TI |

---

## Comunicação

| Canal | Uso |
|---|---|
| **WhatsApp Business** | Atendimento ao paciente, agendamentos e automações |
| **E-mail institucional** | contato@clinicaapice.com.br |

---

## Repositórios na organização

| Repositório | Descrição |
|---|---|
| [APICE-Tecnology/.github](https://github.com/APICE-Tecnology/.github) | Documentação técnica central da apice |
| [APICE-Tecnology/PAINEL-TOTEM](https://github.com/APICE-Tecnology/PAINEL-TOTEM) | Automação de painéis e totems de atendimento |

---

[← Voltar ao início](../README.md)
