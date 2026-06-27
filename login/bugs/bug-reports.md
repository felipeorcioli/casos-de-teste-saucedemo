# Bug Reports — Saucedemo

## BUG001 — Filtro de produtos não funciona

| Campo | Descrição |
|---|---|
| **Pré-condição** | Estar logado com o usuário `problem_user` |
| **Severidade** | Alta |
| **Status** | ❌ Aberto |

**Passos para reproduzir:**
1. Acessar https://www.saucedemo.com
2. Fazer login com `problem_user` / `secret_sauce`
3. Na página de produtos, selecionar o filtro "Price (low to high)"
4. Observar a ordem dos produtos

**Resultado esperado:** Produtos reordenados por preço do menor para o maior

**Resultado obtido:** Produtos permanecem na ordem original, filtro não surte efeito

---

## BUG002 — Imagens dos produtos incompatíveis

| Campo | Descrição |
|---|---|
| **Pré-condição** | Estar logado com o usuário `problem_user` |
| **Severidade** | Alta |
| **Status** | ❌ Aberto |

**Passos para reproduzir:**
1. Acessar https://www.saucedemo.com
2. Fazer login com `problem_user` / `secret_sauce`
3. Observar as imagens dos produtos na página de catálogo

**Resultado esperado:** Cada produto exibe sua imagem correta

**Resultado obtido:** Todos os produtos exibem imagens incorretas, sem relação com o produto

---

## BUG003 — Campo Last Name sobrescreve o campo First Name no checkout

| Campo | Descrição |
|---|---|
| **Pré-condição** | Estar logado com o usuário `problem_user` e estar na página "Checkout: Your Information" |
| **Severidade** | Crítica |
| **Status** | ❌ Aberto |

**Passos para reproduzir:**
1. Fazer login com `problem_user` / `secret_sauce`
2. Adicionar qualquer produto ao carrinho
3. Clicar no carrinho e depois em "Checkout"
4. Digitar qualquer texto no campo "First Name"
5. Digitar qualquer texto no campo "Last Name"

**Resultado esperado:** Cada campo mantém seu próprio valor independentemente

**Resultado obtido:** Ao digitar no campo "Last Name", o conteúdo sobrescreve o campo "First Name", impossibilitando avançar no checkout

---

## BUG004 — Checkout liberado com carrinho vazio

| Campo | Descrição |
|---|---|
| **Pré-condição** | Estar logado com qualquer usuário e com o carrinho vazio |
| **Severidade** | Alta |
| **Status** | ❌ Aberto |

**Passos para reproduzir:**
1. Fazer login com `standard_user` / `secret_sauce`
2. Não adicionar nenhum produto ao carrinho
3. Clicar no ícone do carrinho
4. Clicar em "Checkout"

**Resultado esperado:** Sistema deve exibir mensagem de erro impedindo o checkout sem itens

**Resultado obtido:** Sistema permite avançar para o checkout mesmo com o carrinho vazio
