# Plano de Testes — ShopQA

## 1. Identificação

**Projeto:** ShopQA
**Tipo:** Loja virtual
**Área:** Quality Assurance
**Versão:** 1.0

---

## 2. Objetivo

Este plano de testes tem como objetivo definir a estratégia utilizada para validar as principais funcionalidades do sistema ShopQA, identificando possíveis falhas e garantindo que o sistema atenda aos requisitos funcionais e às regras de negócio definidas.

---

## 3. Escopo

Serão testadas as seguintes funcionalidades:

* Cadastro de usuários
* Login
* Logout
* Listagem de produtos
* Pesquisa de produtos
* Carrinho de compras
* Checkout
* Visualização de pedidos
* Funcionalidades administrativas

---

## 4. Fora do escopo

Neste primeiro ciclo de testes não serão avaliados:

* Desempenho em larga escala
* Testes de carga
* Testes de stress
* Segurança avançada
* Infraestrutura do servidor
* Compatibilidade com dispositivos físicos específicos

Esses testes poderão ser considerados em ciclos futuros.

---

## 5. Tipos de teste

Serão utilizados os seguintes tipos de teste:

### Testes funcionais

Verificar se as funcionalidades do sistema funcionam de acordo com os requisitos definidos.

### Testes negativos

Verificar o comportamento do sistema quando são fornecidos dados inválidos, incompletos ou inesperados.

### Testes exploratórios

Explorar o sistema de forma livre buscando comportamentos inesperados que não estejam necessariamente previstos nos casos de teste.

### Testes de regressão

Verificar se alterações realizadas no sistema não afetaram funcionalidades que anteriormente estavam funcionando.

### Testes de API

Validar as APIs responsáveis pela comunicação entre o sistema e seus serviços.

### Testes automatizados

Automatizar cenários considerados críticos ou repetitivos.

---

## 6. Estratégia de testes

Os testes serão realizados inicialmente de forma manual.

Os cenários serão priorizados de acordo com o impacto que uma possível falha pode causar ao usuário e ao negócio.

As funcionalidades relacionadas a autenticação, carrinho e checkout terão prioridade alta devido ao impacto direto na utilização e no processo de compra.

Após a execução dos testes manuais, os principais cenários poderão ser selecionados para automação.

---

## 7. Priorização

### Alta prioridade

* Cadastro
* Login
* Adicionar produto ao carrinho
* Alterar quantidade no carrinho
* Checkout
* Finalização da compra

### Média prioridade

* Pesquisa de produtos
* Filtros
* Visualização de pedidos
* Administração de produtos

### Baixa prioridade

* Logout
* Elementos visuais não críticos
* Informações complementares dos produtos

---

## 8. Ambiente de testes

Os testes serão realizados inicialmente em ambiente de testes utilizando:

**Sistema operacional:** Windows

**Navegador principal:** Google Chrome

**Testes de API:** Postman

**Automação:** Java + Selenium + JUnit

**Controle de versão:** Git + GitHub

As versões específicas das ferramentas serão registradas conforme o projeto evoluir.

---

## 9. Critérios de entrada

Os testes poderão ser iniciados quando:

* O ambiente de testes estiver disponível;
* As funcionalidades previstas estiverem implementadas;
* Os requisitos estiverem definidos;
* Os dados necessários para os testes estiverem disponíveis.

---

## 10. Critérios de saída

O ciclo de testes poderá ser encerrado quando:

* Os casos de teste planejados forem executados;
* Os principais cenários críticos forem validados;
* Os bugs encontrados forem documentados;
* Os resultados dos testes forem registrados;
* Não existirem defeitos críticos conhecidos sem tratamento.

---

## 11. Riscos

Os principais riscos identificados são:

* Alterações frequentes no sistema durante os testes;
* Ambiente de testes indisponível;
* Requisitos incompletos ou alterados;
* Falta de dados adequados para execução dos testes;
* Bugs bloqueando a execução de outros cenários.

---

## 12. Entregáveis

Ao final do ciclo de testes serão produzidos:

* Plano de testes;
* Casos de teste;
* Cenários BDD;
* Relatório de bugs;
* Evidências dos testes;
* Collection de testes de API;
* Scripts de automação;
* Relatório final de testes.

---

## 13. Ferramentas

As principais ferramentas utilizadas no projeto serão:

* GitHub
* Git
* Postman
* Java
* Selenium
* JUnit

Outras ferramentas poderão ser adicionadas conforme a evolução do projeto.
