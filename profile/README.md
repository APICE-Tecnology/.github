<div align="center">

![apice](https://utils.storage.apicesaudemental.link/capa-ti.png)

# apice — assistência psiquiátrica integral e centro de estudos

*Porque a vida pode ser melhor.*

Salvador, Bahia, Brasil

[![Chamados](https://img.shields.io/badge/chamados-ClickUp-7B68EE?logo=clickup&logoColor=white)](https://clickup.com/)
[![Licença](https://img.shields.io/badge/Licença-Restrita_APICE-blue?logo=opensourceinitiative&logoColor=white)](https://github.com/APICE-Tecnology/.github/blob/main/LICENSE)
[![LGPD](https://img.shields.io/badge/LGPD-Lei_13.709%2F2018-2E7D32)](https://github.com/APICE-Tecnology/.github/blob/main/docs/seguranca.md)
![Maintained](https://img.shields.io/badge/maintained-yes-brightgreen)

</div>

---

## Stack

<div align="center">

![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?logo=cloudflare&logoColor=white)
![Cloudflare Pages](https://img.shields.io/badge/Cloudflare_Pages-F38020?logo=cloudflare&logoColor=white)
![Cloudflare R2](https://img.shields.io/badge/Cloudflare_R2-F38020?logo=cloudflare&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?logo=microsoftsqlserver&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![Pixeon Smart](https://img.shields.io/badge/ERP%2FPEP-Pixeon_Smart-0066CC)
![Wellon](https://img.shields.io/badge/integração-Wellon-00A86B)
![Zerodox](https://img.shields.io/badge/integração-Zerodox-6B21A8)

</div>

---

## Arquitetura

| Camada | Tecnologia | Função |
|---|---|---|
| Edge | Cloudflare Workers | APIs serverless na borda da rede global |
| Frontend | Cloudflare Pages · React · Vite · Tailwind | Interfaces via CDN com deploy contínuo |
| Armazenamento | Cloudflare R2 | Objetos, assets, relatórios, vídeos |
| Banco principal | Supabase (PostgreSQL) + Hyperdrive | Transacional, auth JWT, pool de conexões |
| Banco clínico | SQL Server (rede local) | Smart Pixeon — prontuário e histórico legado |
| Cache | Redis | Filas e processamento assíncrono |
| ERP/PEP | Smart Pixeon · Wellon · Zerodox | Prontuário eletrônico, agenda, integrações clínicas |

---

## Sistemas em produção

| Sistema | Tecnologia | Função |
|---|---|---|
| **CISSA** | Workers + Supabase + RAG | IA institucional — triagem, chat, base de conhecimento |
| **PAINEL-TOTEM** | Scripts locais + Smart API | Chamada de pacientes e totems de autoatendimento |
| **Instituto apice** | Cloudflare Pages | Portal de formação — [institutoapice.org.br](https://institutoapice.org.br) |

---

## Repositórios

| Repositório | Descrição |
|---|---|
| [.github](https://github.com/APICE-Tecnology/.github) | Documentação técnica da organização |
| [PAINEL-TOTEM](https://github.com/APICE-Tecnology/PAINEL-TOTEM) | Automação de painéis e totems de atendimento |

---

<div align="center">

[clinicaapice.com.br](https://clinicaapice.com.br) · ti.clinicaapice@gmail.com · +55 71 3028-8350

</div>
