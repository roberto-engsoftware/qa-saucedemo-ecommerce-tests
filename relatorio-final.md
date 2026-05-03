# Relatório Final de Testes — SauceDemo

## Projeto

Testes manuais em fluxo de e-commerce no SauceDemo.

## Objetivo

Validar as principais funcionalidades de um fluxo de compra em um e-commerce demo, incluindo login, visualização de produtos, carrinho, checkout, validação de campos obrigatórios, finalização da compra e logout.

## Resumo da execução

Foram executados 14 casos de teste manuais, contemplando cenários positivos e negativos.

Durante a execução, a maior parte dos cenários apresentou comportamento conforme esperado. No entanto, foi identificado 1 bug no fluxo de finalização de compra, relacionado ao caso de teste CT-013.

---

## Resultado geral

| Total de casos | Aprovados | Reprovados | Bloqueados | Não executados |
|---|---:|---:|---:|---:|
| 14 | 13 | 1 | 0 | 0 |

---

## Casos reprovados

| ID | Cenário | Resultado |
|---|---|---|
| CT-013 | Finalizar compra | Reprovado |

---

## Bug identificado

**BUG-001 — Erro ao finalizar compra no checkout**

Durante a execução do caso de teste **CT-013 — Finalizar compra**, ao clicar no botão **Finish**, o sistema retornou para a tela de login e exibiu uma mensagem informando que somente é possível acessar o checkout com uma conta autenticada.

Esse comportamento ocorreu mesmo com o usuário já estando logado e com uma conta associada durante o fluxo de checkout.

### Resultado esperado

O sistema deveria concluir a compra e exibir a mensagem de sucesso.

### Resultado obtido

O sistema retornou para a tela de login e exibiu mensagem de erro relacionada à autenticação.

### Impacto

O bug impacta diretamente o fluxo principal de compra, pois impede a finalização do pedido.

### Severidade

Alta

### Prioridade

Alta

### Evidência

`evidencias/CT-013-compra-finalizada-bug.png`

---

## Funcionalidades testadas

- Login
- Produtos
- Carrinho
- Checkout
- Validação de campos obrigatórios
- Resumo da compra
- Finalização do pedido
- Logout

---

## Evidências

As evidências foram registradas por meio de capturas de tela durante a execução dos testes e armazenadas na pasta `/evidencias`.

Principais evidências registradas:

- `CT-001-login-usuario-valido.png`
- `CT-002-usuario-bloqueado.png`
- `CT-003-login-campos-vazios.png`
- `CT-004-senha-invalida.png`
- `CT-005-lista-produtos.png`
- `CT-006-produto-adicionado-carrinho.png`
- `CT-007-produto-removido-carrinho.png`
- `CT-008-tela-carrinho.png`
- `CT-009-tela-checkout.png`
- `CT-010-checkout-campos-vazios.png`
- `CT-011-checkout-preenchido.png`
- `CT-012-validacao-preco-total.png`
- `CT-013-compra-finalizada-bug.png`
- `CT-014-logout.png`

---

## Conclusão

Foram executados 14 casos de teste manuais no fluxo de e-commerce do SauceDemo.

Dos casos executados, 13 foram aprovados e 1 foi reprovado. O caso reprovado foi o **CT-013 — Finalizar compra**, no qual o sistema retornou para a tela de login ao tentar concluir o pedido, mesmo com o usuário autenticado durante o fluxo.

Esse comportamento representa uma falha importante, pois impede a conclusão da compra e afeta diretamente a experiência do usuário.

O projeto contribuiu para a prática de planejamento de testes, execução manual, análise de resultado esperado versus resultado obtido, registro de evidências e documentação de bugs em um cenário próximo de uma rotina real de Quality Assurance.