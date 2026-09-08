# Casos de Teste — ShopQA

## Legenda

| Prioridade | Descrição                                  |
| ---------- | ------------------------------------------ |
| Alta       | Funcionalidade crítica para o sistema      |
| Média      | Funcionalidade importante, mas não crítica |
| Baixa      | Funcionalidade de menor impacto            |

| Status        | Descrição                          |
| ------------- | ---------------------------------- |
| Não executado | Teste ainda não realizado          |
| Aprovado      | Resultado obtido conforme esperado |
| Reprovado     | Resultado diferente do esperado    |
| Bloqueado     | Não foi possível executar o teste  |

---

# 1. Cadastro

## CT-001 — Cadastro com dados válidos

**Requisito:** RF01
**Prioridade:** Alta
**Tipo:** Funcional

### Pré-condições

* Usuário não possui cadastro no sistema.

### Dados de teste

* Nome: João da Silva
* E-mail: [joao.teste@example.com](mailto:joao.teste@example.com)
* Senha: Teste@123
* Confirmação: Teste@123

### Passos

1. Acessar a página de cadastro.
2. Informar o nome.
3. Informar um e-mail válido.
4. Informar uma senha válida.
5. Confirmar a senha.
6. Clicar em "Cadastrar".

### Resultado esperado

O sistema deve criar a conta e informar que o cadastro foi realizado com sucesso.

**Status:** Não executado

---

## CT-002 — Cadastro com e-mail já existente

**Requisito:** RF01 / RN01
**Prioridade:** Alta
**Tipo:** Negativo

### Pré-condições

* O e-mail informado já está cadastrado no sistema.

### Passos

1. Acessar a página de cadastro.
2. Informar dados válidos.
3. Informar um e-mail já cadastrado.
4. Clicar em "Cadastrar".

### Resultado esperado

O sistema deve impedir o cadastro e informar que o e-mail já está sendo utilizado.

**Status:** Não executado

---

## CT-003 — Cadastro com senhas diferentes

**Requisito:** RF01 / RN03
**Prioridade:** Alta
**Tipo:** Negativo

### Passos

1. Acessar a página de cadastro.
2. Informar nome válido.
3. Informar e-mail válido.
4. Informar uma senha.
5. Informar uma confirmação de senha diferente.
6. Clicar em "Cadastrar".

### Resultado esperado

O sistema deve impedir o cadastro e informar que as senhas não são iguais.

**Status:** Não executado

---

# 2. Login

## CT-004 — Login com credenciais válidas

**Requisito:** RF02
**Prioridade:** Alta
**Tipo:** Funcional

### Pré-condições

* Usuário possui cadastro válido.

### Passos

1. Acessar a página de login.
2. Informar e-mail válido.
3. Informar senha válida.
4. Clicar em "Entrar".

### Resultado esperado

O sistema deve autenticar o usuário e direcioná-lo para a área autenticada.

**Status:** Aprovado

**Resultado obtido:** O usuário foi autenticado com sucesso e conseguiu acessar a área de produtos.

---

## CT-005 — Login com senha incorreta

**Requisito:** RF02 / RN04
**Prioridade:** Alta
**Tipo:** Negativo

### Passos

1. Acessar a página de login.
2. Informar um e-mail cadastrado.
3. Informar uma senha incorreta.
4. Clicar em "Entrar".

### Resultado esperado

O sistema não deve permitir o acesso e deve apresentar uma mensagem informando que as credenciais são inválidas.

**Status:** Não executado

---

## CT-006 — Login com campos vazios

**Requisito:** RF02
**Prioridade:** Alta
**Tipo:** Negativo

### Passos

1. Acessar a página de login.
2. Deixar o campo de e-mail vazio.
3. Deixar o campo de senha vazio.
4. Clicar em "Entrar".

### Resultado esperado

O sistema deve impedir o login e informar que os campos obrigatórios devem ser preenchidos.

**Status:** Não executado

---

# 3. Produtos

## CT-007 — Visualizar lista de produtos

**Requisito:** RF03
**Prioridade:** Média
**Tipo:** Funcional

### Passos

1. Acessar a loja.
2. Acessar a área de produtos.

### Resultado esperado

O sistema deve apresentar os produtos disponíveis com nome, imagem, preço, descrição e disponibilidade.

**Status:** Não executado

---

## CT-008 — Pesquisar produto existente

**Requisito:** RF04
**Prioridade:** Média
**Tipo:** Funcional

### Passos

1. Acessar a loja.
2. Localizar o campo de pesquisa.
3. Informar "Notebook".
4. Executar a pesquisa.

### Resultado esperado

O sistema deve apresentar produtos relacionados ao termo pesquisado.

**Status:** Não executado

---

## CT-009 — Pesquisar produto inexistente

**Requisito:** RF04
**Prioridade:** Média
**Tipo:** Negativo

### Passos

1. Acessar a loja.
2. Informar um termo que não corresponda a nenhum produto.
3. Executar a pesquisa.

### Resultado esperado

O sistema deve informar que nenhum produto foi encontrado.

**Status:** Não executado

---

# 4. Carrinho

## CT-010 — Adicionar produto ao carrinho

**Requisito:** RF05
**Prioridade:** Alta
**Tipo:** Funcional

### Passos

1. Acessar a lista de produtos.
2. Selecionar um produto disponível.
3. Clicar em "Adicionar ao carrinho".
4. Acessar o carrinho.

### Resultado esperado

O produto deve ser adicionado ao carrinho e seu preço deve ser apresentado corretamente.

**Status:** Não executado

---

## CT-011 — Alterar quantidade do produto

**Requisito:** RF05 / RN06
**Prioridade:** Alta
**Tipo:** Funcional

### Pré-condições

* Existe um produto no carrinho.

### Passos

1. Acessar o carrinho.
2. Alterar a quantidade do produto para 2.
3. Verificar o subtotal.

### Resultado esperado

A quantidade deve ser alterada e o subtotal deve ser recalculado corretamente.

**Status:** Não executado

---

## CT-012 — Remover produto do carrinho

**Requisito:** RF05
**Prioridade:** Alta
**Tipo:** Funcional

### Pré-condições

* Existe um produto no carrinho.

### Passos

1. Acessar o carrinho.
2. Clicar em "Remover" no produto.

### Resultado esperado

O produto deve ser removido e o valor total deve ser atualizado.

**Status:** Não executado

---

# 5. Checkout

## CT-013 — Finalizar compra com dados válidos

**Requisito:** RF06 / RN08
**Prioridade:** Alta
**Tipo:** Funcional

### Pré-condições

* Usuário autenticado.
* Existe produto no carrinho.

### Passos

1. Acessar o carrinho.
2. Clicar em "Finalizar compra".
3. Informar os dados de entrega.
4. Informar os dados de pagamento.
5. Confirmar a compra.

### Resultado esperado

A compra deve ser processada e um novo pedido deve ser criado.

**Status:** Não executado

---

# 6. Pedidos

## CT-014 — Visualizar pedido realizado

**Requisito:** RF07
**Prioridade:** Média
**Tipo:** Funcional

### Pré-condições

* Usuário possui pelo menos um pedido realizado.

### Passos

1. Acessar a conta do usuário.
2. Acessar "Meus pedidos".
3. Selecionar um pedido.

### Resultado esperado

O sistema deve apresentar o número do pedido, data, produtos, quantidade, valor e status.

**Status:** Não executado

---

# 7. Logout

## CT-015 — Realizar logout

**Requisito:** RF08 / RN10
**Prioridade:** Média
**Tipo:** Funcional

### Pré-condições

* Usuário está autenticado.

### Passos

1. Acessar a área autenticada.
2. Clicar em "Sair".

### Resultado esperado

O usuário deve ser desconectado e não deve conseguir acessar páginas restritas sem realizar novo login.

**Status:** Não executado
