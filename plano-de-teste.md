
Esse arquivo mostra o **planejamento** antes de executar.

# Plano de Teste — SauceDemo

## 1. Objetivo

Validar as principais funcionalidades de um fluxo de compra em um e-commerce demo, garantindo que o usuário consiga realizar login, visualizar produtos, adicionar itens ao carrinho, preencher o checkout e finalizar uma compra com sucesso.

## 2. Escopo dos testes

Serão testadas as seguintes funcionalidades:

- Login com credenciais válidas
- Login com credenciais inválidas
- Login com usuário bloqueado
- Listagem de produtos
- Adição de produto ao carrinho
- Remoção de produto do carrinho
- Validação da quantidade de itens no carrinho
- Acesso ao carrinho
- Preenchimento do checkout
- Validação de campos obrigatórios
- Resumo da compra
- Finalização da compra
- Logout

## 3. Fora do escopo

Não serão testados:

- Integração com pagamento real
- Performance da aplicação
- Segurança avançada
- Testes automatizados
- Testes em dispositivos móveis
- Integração com banco de dados

## 4. Ambiente de teste

- Site: SauceDemo
- URL: https://www.saucedemo.com/
- Navegador: Brave
- Sistema operacional: Windows 10
- Tipo de teste: Manual

## 5. Dados de teste

Usuário válido:

- Username: standard_user
- Password: secret_sauce

Usuário bloqueado:

- Username: locked_out_user
- Password: secret_sauce

Usuário problemático:

- Username: problem_user
- Password: secret_sauce

## 6. Critérios de entrada

- Site acessível
- Navegador funcionando corretamente
- Credenciais disponíveis
- Conexão com internet ativa

## 7. Critérios de saída

- Todos os casos de teste foram executados
- Evidências foram registradas
- Resultados foram atualizados
- Relatório final foi elaborado

## 8. Riscos

- Instabilidade do site demo
- Mudança nas credenciais de acesso
- Alterações na interface do sistema