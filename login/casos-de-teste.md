# Casos de Teste — Login

## CT001 — Login com sucesso

| Campo | Descrição |
|---|---|
| **Pré-condição** | Estar na página de login do Saucedemo |
| **Resultado esperado** | Usuário redirecionado para a página de produtos |
| **Severidade** | — |

**Passos:**
1. Acessar https://www.saucedemo.com
2. Preencher o campo usuário com `standard_user`
3. Preencher o campo senha com `secret_sauce`
4. Clicar em "Login"

**Resultado obtido:** ✅ Passou

---

## CT002 — Login com senha incorreta

| Campo | Descrição |
|---|---|
| **Pré-condição** | Estar na página de login do Saucedemo |
| **Resultado esperado** | Sistema exibe mensagem "Username and password do not match any user in this service" e permanece na página de login |
| **Severidade** | Alta |

**Passos:**
1. Acessar https://www.saucedemo.com
2. Preencher o campo usuário com `standard_user`
3. Preencher o campo senha com `123456`
4. Clicar em "Login"

**Resultado obtido:** ✅ Passou

---

## CT003 — Login com usuário bloqueado

| Campo | Descrição |
|---|---|
| **Pré-condição** | Estar na página de login do Saucedemo |
| **Resultado esperado** | Sistema exibe mensagem "Sorry, this user has been locked out" e permanece na página de login |
| **Severidade** | Alta |

**Passos:**
1. Acessar https://www.saucedemo.com
2. Preencher o campo usuário com `locked_out_user`
3. Preencher o campo senha com `secret_sauce`
4. Clicar em "Login"

**Resultado obtido:** ✅ Passou
