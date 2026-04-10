![Documentação TI](https://utils.storage.apicesaudemental.link/documentacao-ti.png)

# Contribuindo — GitHub APICE

Como usar o GitHub da organização, abrir issues, criar pull requests e manter os repositórios organizados.

---

## Organização

Todos os repositórios da empresa ficam em **[github.com/APICE-Tecnology](https://github.com/APICE-Tecnology)**.

Repositórios criados em contas pessoais devem ser transferidos para a organização assim que possível (veja instruções abaixo).

---

## Abrindo uma Issue

Use issues para registrar problemas, solicitações e melhorias. Cada repositório tem templates pré-configurados.

| Template | Quando usar |
|---|---|
| **Bug Report** | Algo não funciona como esperado — descreva o comportamento e o impacto |
| **Feature Request** | Sugestão de nova funcionalidade ou melhoria |
| **Suporte Clínico/Operacional** | Dúvidas sobre fluxo, painel, agenda ou sistema clínico |

**Como abrir:**
1. Acesse o repositório no GitHub
2. Clique em **Issues → New Issue**
3. Selecione o template adequado
4. Preencha todos os campos e submeta

> Issues são automaticamente atribuídas ao responsável de TI via workflow de auto-assign.

---

## Fluxo de trabalho — Pull Request

Para qualquer alteração em código ou documentação:

1. **Crie uma branch** com nome descritivo a partir de `main`

   ```
   git checkout -b tipo/descricao-curta
   ```

   Exemplos:
   ```
   fix/cookie-totem-1-andar
   feat/cissa-prompt-triagem
   docs/infraestrutura-wellon
   ```

2. **Faça as alterações** e commite seguindo o padrão:

   ```
   tipo: descrição objetiva do que foi feito
   ```

   Tipos válidos: `fix`, `feat`, `docs`, `refactor`, `chore`, `infra`

3. **Abra o Pull Request** para `main` — o template de PR aparece automaticamente

4. **Aguarde revisão** do responsável antes de fazer merge

---

## Padrão de nomenclatura de repositórios

| Tipo | Formato | Exemplo |
|---|---|---|
| Sistema ou produto | `NOME-SISTEMA` | `PAINEL-TOTEM`, `CISSA-BACKEND` |
| Documentação | `docs-NOME` | `docs-protocolos` |
| Infraestrutura | `infra-NOME` | `infra-cloudflare` |

Use letras maiúsculas para repositórios de sistemas e lowercase com hífen para scripts e documentação.

---

## Transferindo repositório pessoal para a organização

Para mover um repositório de uma conta pessoal para `APICE-Tecnology`:

1. Acesse o repositório no GitHub
2. Vá em **Settings → Danger Zone → Transfer ownership**
3. Confirme digitando o nome do repositório
4. Selecione **APICE-Tecnology** como destino
5. Confirme a transferência

> O link antigo redireciona automaticamente por um período. Atualize referências internas após a transferência.

---

## Regras de segurança nos repositórios

- **Nunca** commite credenciais, tokens, chaves de API ou senhas — em nenhum arquivo, em nenhuma branch
- Configure as credenciais como **GitHub Secrets** em workflows de Actions
- Sempre inclua `.env` e arquivos sensíveis no `.gitignore` antes do primeiro commit
- Se uma credencial for exposta: revogue imediatamente e notifique o TI

---

## Contato de TI

Para dúvidas, acesso ao GitHub da organização ou configuração de repositórios:

- WhatsApp: **+55 71 3028-8350**
- E-mail: **ti.clinicaapice@gmail.com**

---

[← Voltar ao início](../README.md)
