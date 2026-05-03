# Casos de Teste — SauceDemo

## Informações gerais

**Projeto:** Testes Manuais no SauceDemo  
**Tipo de teste:** Manual  
**Site testado:** https://www.saucedemo.com/  
**Ambiente:** Brave — Windows 10
**Responsável:** Roberto Rodrigues  

---

# CT-001 — Login com usuário válido

**Funcionalidade:** Login  
**Pré-condição:** Estar na tela de login  

**Dados de teste:**

- Usuário: `standard_user`
- Senha: `secret_sauce`

**Passos:**

1. Acessar o site SauceDemo
2. Informar o usuário válido
3. Informar a senha válida
4. Clicar no botão Login

**Resultado esperado:**  
O sistema deve redirecionar o usuário para a tela de produtos.

**Resultado obtido:**  
O sistema redirecionou corretamente a tela de produtos.

**Status:** Aprovado

---

# CT-002 — Login com usuário bloqueado

**Funcionalidade:** Login  
**Pré-condição:** Estar na tela de login  

**Dados de teste:**

- Usuário: `locked_out_user`
- Senha: `secret_sauce`

**Passos:**

1. Acessar o site SauceDemo
2. Informar o usuário bloqueado
3. Informar a senha válida
4. Clicar no botão Login

**Resultado esperado:**  
O sistema deve exibir uma mensagem informando que o usuário está bloqueado.

**Resultado obtido:**  
Mensagem de usuário bloqueado apareceu corretamente

**Status:** Aprovado

---

# CT-003 — Login com campos vazios

**Funcionalidade:** Login  
**Pré-condição:** Estar na tela de login  

**Dados de teste:**

- Usuário: vazio
- Senha: vazia

**Passos:**

1. Acessar o site SauceDemo
2. Deixar os campos usuário e senha vazios
3. Clicar no botão Login

**Resultado esperado:**  
O sistema deve exibir mensagem informando que o campo usuário é obrigatório.

**Resultado obtido:**  
Sistema exibiu mensagem informando que é obrigatório o preenchimento dos campos.

**Status:** Aprovado

---

# CT-004 — Login com senha inválida

**Funcionalidade:** Login  
**Pré-condição:** Estar na tela de login  

**Dados de teste:**

- Usuário: `standard_user`
- Senha: `senha_errada`

**Passos:**

1. Acessar o site SauceDemo
2. Informar o usuário válido
3. Informar uma senha inválida
4. Clicar no botão Login

**Resultado esperado:**  
O sistema deve exibir mensagem de erro para credenciais inválidas.

**Resultado obtido:**  
 Sistema informou que as credenciais estavam inválidas

**Status:** Aprovado

---

# CT-005 — Visualizar lista de produtos

**Funcionalidade:** Produtos  
**Pré-condição:** Estar logado no sistema  

**Dados de teste:**

- Usuário: `standard_user`
- Senha: `secret_sauce`

**Passos:**

1. Realizar login com credenciais válidas
2. Verificar a tela principal de produtos

**Resultado esperado:**  
O sistema deve exibir a lista de produtos disponíveis.

**Resultado obtido:**  
A lista de produtos apareceu corretamente 

**Status:** Aprovado

---

# CT-006 — Adicionar produto ao carrinho

**Funcionalidade:** Carrinho  
**Pré-condição:** Estar logado na tela de produtos  

**Dados de teste:**

- Produto: Sauce Labs Backpack

**Passos:**

1. Localizar o produto Sauce Labs Backpack
2. Clicar em Add to cart

**Resultado esperado:**  
O produto deve ser adicionado ao carrinho e o contador deve ser atualizado.

**Resultado obtido:**   Produto adicionado corretamente e contador atualizado corretamente 

**Status:** Aprovado

---

# CT-007 — Remover produto do carrinho

**Funcionalidade:** Carrinho  
**Pré-condição:** Ter um produto adicionado ao carrinho  

**Dados de teste:**

- Produto: Sauce Labs Backpack

**Passos:**

1. Adicionar o produto ao carrinho
2. Clicar em Remove

**Resultado esperado:**  
O produto deve ser removido e o contador do carrinho deve ser atualizado.

**Resultado obtido:**  
Produto removido e contador do carrinho atualizado corretamente.

**Status:** Aprovado

---

# CT-008 — Acessar o carrinho

**Funcionalidade:** Carrinho  
**Pré-condição:** Ter produto adicionado ao carrinho  

**Dados de teste:**

- Produto: Sauce Labs Backpack

**Passos:**

1. Adicionar produto ao carrinho
2. Clicar no ícone do carrinho

**Resultado esperado:**  
O sistema deve exibir a tela do carrinho com o produto selecionado.

**Resultado obtido:**  
Produto adicionado corretamente.

**Status:** Aprovado

---

# CT-009 — Iniciar checkout

**Funcionalidade:** Checkout  
**Pré-condição:** Ter produto no carrinho  

**Dados de teste:**

- Produto: Sauce Labs Backpack

**Passos:**

1. Acessar o carrinho
2. Clicar em Checkout

**Resultado esperado:**  
O sistema deve exibir o formulário de informações do cliente.

**Resultado obtido:**  
Exibiu formulario corretamente

**Status:** Aprovado

---

# CT-010 — Checkout com campos vazios

**Funcionalidade:** Checkout  
**Pré-condição:** Estar na tela de checkout  

**Dados de teste:**

- Nome: vazio
- Sobrenome: vazio
- CEP: vazio

**Passos:**

1. Acessar a tela de checkout
2. Deixar todos os campos vazios
3. Clicar em Continue

**Resultado esperado:**  
O sistema deve exibir mensagem de erro para campo obrigatório.

**Resultado obtido:**  
 Sistema exibiu mensagem de erro ao executar o teste.

**Status:** Aprovado

---

# CT-011 — Preencher checkout corretamente

**Funcionalidade:** Checkout  
**Pré-condição:** Estar na tela de checkout  

**Dados de teste:**

- Nome: Roberto
- Sobrenome: Rodrigues
- CEP: 69000-000

**Passos:**

1. Preencher o campo Nome
2. Preencher o campo Sobrenome
3. Preencher o campo CEP
4. Clicar em Continue

**Resultado esperado:**  
O sistema deve avançar para a tela de resumo da compra.

**Resultado obtido:**  
 Sistema avançou para tela de resumo de compra.

**Status:** Aprovado

---

# CT-012 — Validar preço total

**Funcionalidade:** Checkout  
**Pré-condição:** Estar na tela de resumo da compra  

**Dados de teste:**

- Produto: Sauce Labs Backpack

**Passos:**

1. Verificar o subtotal
2. Verificar a taxa
3. Comparar com o valor total exibido

**Resultado esperado:**  
O total deve corresponder à soma do subtotal com a taxa.

**Resultado obtido:**  
Total corresponde exatamente ao subtotal com a taxa.

**Status:** Aprovado

---

# CT-013 — Finalizar compra

**Funcionalidade:** Checkout  
**Pré-condição:** Estar na tela de resumo da compra  

**Dados de teste:**

- Produto: Sauce Labs Backpack

**Passos:**

1. Estar na tela de resumo da compra
2. Clicar em Finish

**Resultado esperado:**  
O sistema deve exibir mensagem de compra concluída com sucesso.

**Resultado obtido:**  
Sistema voltou a tela de login com mensagem de erro informando que so pode acessar o checkout com uma conta de acesso, porem na tela de checkout ja estava com uma aconta associada.

**Status:** Reprovado

---

# CT-014 — Logout do sistema

**Funcionalidade:** Logout  
**Pré-condição:** Estar logado no sistema  

**Dados de teste:**

- Usuário: `standard_user`

**Passos:**

1. Abrir o menu lateral
2. Clicar em Logout

**Resultado esperado:**  
O sistema deve retornar para a tela de login.

**Resultado obtido:**  
Sistema voltou para tela de login.

**Status:** Aprovado

---

# Legenda de status

| Status | Descrição |
|---|---|
| Não Executado | Caso de teste ainda não foi Executado |
| Aprovado | Resultado obtido foi igual ao resultado esperado |
| Reprovado | Resultado obtido foi diferente do resultado esperado |
| Bloqueado | Não foi possível executar o caso de teste |