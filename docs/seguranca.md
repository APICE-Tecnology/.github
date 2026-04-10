![Documentação TI](https://utils.storage.apicesaudemental.link/documentacao-ti.png)

# Segurança e LGPD — apice

Regras de acesso, proteção de dados de saúde e procedimentos para incidentes.

---

## Controle de acesso

O acesso a todos os sistemas da apice é gerenciado por **nível de permissão** e **unidade de atuação**. Cada colaborador acessa apenas o necessário para suas funções.

| Nível | Perfil | Acesso |
|---|---|---|
| **Administrador** | TI / Gestão geral | Acesso irrestrito a todos os sistemas |
| **Gestor** | Coordenadores de unidade | Equipe, relatórios e dados da sua unidade |
| **Profissional Clínico** | Médicos, psicólogos | Prontuário, evoluções e prescrições |
| **Apoio Clínico** | Técnicos, enfermagem | Dados do paciente sem acesso a prescrições |
| **Administrativo** | Recepção, secretaria | Agenda, cadastros e dados básicos |
| **Residente / Estudante** | Residentes, alunos | Acesso supervisionado e restrito |

### 2FA — Verificação em duas etapas

Obrigatório para os níveis **Administrador** e **Gestor**.
Configure via Google Authenticator, Authy ou app equivalente.
Em caso de dúvida na configuração, contate o TI.

---

## Senhas

| Regra | Requisito |
|---|---|
| Tamanho mínimo | 12 caracteres |
| Composição | Letras maiúsculas, minúsculas, números e símbolos |
| Validade | 90 dias para administradores e gestores |
| Reutilização | Não reutilize as últimas 5 senhas |
| Bloqueio | Após 5 tentativas erradas — contate o TI para desbloquear |

---

## Proteção de dados — LGPD

A apice opera com **dados sensíveis de saúde**, categoria especial pela LGPD (Lei 13.709/2018). O tratamento é fundamentado no Art. 11, II, f — tutela da saúde por serviços de saúde.

**Regras obrigatórias para todos os colaboradores:**

- Não compartilhe dados de pacientes fora dos sistemas oficiais da apice (Smart, CISSA, Supabase)
- Não tire prints de prontuários e envie por WhatsApp pessoal ou e-mail não institucional
- Acesse apenas os pacientes sob seus cuidados diretos
- Não deixe sessão ativa em computadores compartilhados ou de uso público
- Não discuta dados identificáveis de pacientes em ambientes não seguros

**Prazos de retenção de dados:**

| Tipo | Prazo mínimo | Base legal |
|---|---|---|
| Prontuário médico | 20 anos | Resolução CFM 1.638/2002 |
| Dados de pacientes menores | Até maioridade + 5 anos | ECA + CFM |
| Logs e registros de acesso | 5 anos | Resolução CFM |
| Documentos de cobrança | 5 anos | Código Tributário Nacional |

---

## O que fazer em cada situação

### Esqueceu a senha ou conta bloqueada

Contate o TI imediatamente:
- WhatsApp: **+55 71 3028-8350**
- E-mail: **ti.clinicaapice@gmail.com**

### Suspeita de acesso indevido à sua conta

1. Troque sua senha imediatamente
2. Encerre todas as sessões ativas
3. Notifique o TI com: data, hora, o que foi acessado, se possível
4. Não apague nenhuma evidência (e-mails, prints, logs)

### Incidente com dados de paciente (vazamento ou acesso não autorizado)

1. Notifique o TI em até **2 horas** após a descoberta
2. Não tente resolver sozinho — preserve as evidências
3. Para incidentes graves: comunicação à ANPD em até **72 horas** (responsabilidade da gestão de TI)

---

## Segurança nos repositórios GitHub

Qualquer código ou configuração no GitHub da apice deve seguir estas regras:

- **Jamais** commite tokens de API, senhas, chaves privadas ou credenciais de qualquer tipo
- Use **GitHub Secrets** para credenciais em workflows de CI/CD
- Use **variáveis de ambiente** e arquivos `.env` (nunca versionados) em desenvolvimento local
- Adicione `.env` e arquivos sensíveis ao `.gitignore` antes do primeiro commit

**Se uma credencial for exposta acidentalmente:**
1. Revogue o token/credencial imediatamente no serviço correspondente (Cloudflare, Supabase, GitHub)
2. Notifique o TI
3. Gere uma nova credencial e atualize os secrets

---

[← Voltar ao início](../README.md)
