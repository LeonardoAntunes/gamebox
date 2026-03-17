# 📄 Product Requirements Document (PRD) - Gamebox

## 1. Visão Geral e Objetivo

O **Gamebox** é uma aplicação web didática que visa criar um espaço onde você pode compartilhar a sua experiencia de suas jogatinas e deseja ao decorrer dos jogos mostrar as suas conquistas e fazer reviwes sobre os jogos qual completou.

**O grande diferencial ():**

## 2. Atores do Sistema

- **Visitante:** Usuário não autenticado que acessa a página inicial e deseja abrir uma conta.
- **Reviwer:** Usuário autenticado que consegue realizar postagens, sendo as mesmas reviews, comentarios em outras postagens, compartilhar conquistas e os status atual de sua jogatina(se está jogando atualmente, deu uma pausa ou completou).
- **O Administrador(Sistema):** Ator invisível que monitora os comportamentos da comunidade, agindo quano necessario para ajudar sobre duvidas ou realizar punimentos aos que ferem as diretrizes da comunidade.

## 3. Histórias de Usuário e Escopo

Abaixo estão as funcionalidades principais do MVP (Minimum Viable Product), escritas sob a perspectiva do usuário final.

### 👤 Épico 1: Autenticação e Conta

- **US01 - Abertura de Conta:** Como um Visitante, quero preencher um formulário com meus dados pessoais (Nome, CPF, Senha) para criar uma nova conta no Roubank.
  - _Critérios de Aceitação:_ O CPF deve ser validado; todos os campos são obrigatórios; a conta deve iniciar com saldo R$ 0,00.
- **US02 - Acesso ao Sistema (Login):** Como um Cliente, quero inserir meu CPF e Senha para acessar meu painel financeiro.

### 💰 Épico 2: Movimentações Financeiras

- **US03 - Visualização de Saldo:** Como um Cliente logado, quero ver meu saldo total atualizado em destaque no painel principal, para saber quanto dinheiro (ainda) tenho.
- **US04 - Realizar Depósito:** Como um Cliente, quero informar um valor para depositar na minha conta.
  - _Critérios de Aceitação:_ O valor deve ser positivo; o sistema deve cobrar uma **"Taxa de Depósito" (ex: 2% do valor)** e creditar apenas o valor líquido na conta do cliente.
- **US05 - Realizar Saque:** Como um Cliente, quero informar um valor para sacar da minha conta.
  - _Critérios de Aceitação:_ O cliente não pode sacar mais do que o saldo disponível + limite; o sistema deve cobrar uma **"Taxa de Saque" (ex: R$ 5,00 fixos por saque)**, descontando o valor do saque + a taxa do saldo total.

### 📊 Épico 3: Histórico e Transparência

- **US06 - Visualizar Extrato:** Como um Cliente, quero visualizar uma lista (tabela ou cards) com o histórico de todas as minhas transações (depósitos e saques).
  - _Critérios de Aceitação:_ A lista deve mostrar a data, o tipo de transação, o valor bruto e **o valor da taxa cobrada** pelo Roubank, deixando claro o quanto o cliente perdeu na operação.
