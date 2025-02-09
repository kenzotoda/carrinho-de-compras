# Carrinho de Compras - Vue.js + Supabase

**Autores**:
- Kenzo Ribeiro Toda
- Marcelo Hitoshi Kondo Oya

Este projeto é uma aplicação web simples de carrinho de compras desenvolvida com **Vue.js** para o front-end e **Supabase** como banco de dados. O objetivo do projeto é permitir que os usuários visualizem produtos, adicionem ao carrinho e finalizem compras, com os dados armazenados no banco de dados Supabase.

## Tecnologias Usadas

- **Vue.js**: Framework JavaScript para construir a interface de usuário reativa.
- **jQuery**: Biblioteca JavaScript para facilitar a manipulação do DOM e chamadas AJAX.
- **Bootstrap 4**: Framework CSS para o design responsivo e componentes prontos.
- **Supabase**: Backend como serviço (BaaS) para armazenar dados do carrinho de compras e produtos em um banco de dados PostgreSQL.

## Como o Supabase é utilizado

O **Supabase** foi integrado para fornecer a persistência de dados para o carrinho de compras e os produtos exibidos na interface. Aqui está como o Supabase é utilizado no projeto:

1. **Tabela de Produtos**: Os produtos disponíveis para compra são recuperados a partir de uma tabela no Supabase chamada `produtos`. Ao carregar a página, o sistema faz uma chamada à API do Supabase para buscar todos os produtos registrados e exibi-los para o usuário.

2. **Tabela de Carrinho**: Quando o usuário finaliza a compra, os dados do carrinho (nome e quantidade de cada produto) são enviados para uma tabela chamada `carrinho` no banco de dados Supabase. Isso é feito via uma requisição `POST` para salvar as informações do carrinho no banco.

3. **Autenticação e Autorização**: Para garantir a segurança da comunicação com a API do Supabase, é utilizado um **API Key** e um token de autorização, configurados nos cabeçalhos das requisições, para garantir que o acesso seja restrito e autorizado.

## Pré-requisitos

Antes de rodar o projeto, tenha certeza de que você tem as seguintes dependências instaladas:

- **Navegador Web**: Qualquer navegador moderno, como Google Chrome ou Firefox.
- **Editor de código**: Como [VSCode](https://code.visualstudio.com/) ou qualquer editor de sua escolha.
- **Conta no Supabase**: Você precisa de uma conta no [Supabase](https://supabase.com/) e de um projeto criado lá para configurar as tabelas `produtos` e `carrinho`. 
    - Crie um banco de dados no Supabase e crie as tabelas correspondentes (`produtos` e `carrinho`).
    - Gere a **API Key** e configure a autorização no seu projeto para interagir com a API.

## Como Rodar o Projeto

### 1. Clone o repositório

No terminal, execute o seguinte comando para clonar o repositório para o seu ambiente local:

```bash
git clone https://github.com/kenzotoda/carrinho-de-compras.git
