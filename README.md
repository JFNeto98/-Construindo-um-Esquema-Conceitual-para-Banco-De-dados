# Sistema de Banco de Dados para Oficina Mecânica

## 📌 Descrição da Atividade
Este repositório contém o projeto conceitual de um **banco de dados para uma oficina mecânica**.  

O objetivo da atividade foi modelar as principais entidades, relacionamentos e regras de negócio que estruturam o funcionamento de uma oficina, permitindo o controle de **clientes, veículos, ordens de serviço, serviços realizados, produtos, mecânicos e estoque**.

---

## 🎯 Objetivos da Modelagem
- Cadastrar e gerenciar **clientes** (Pessoa Física ou Jurídica).  
- Associar **veículos aos clientes**, com informações de marca, modelo e placa.  
- Registrar **ordens de serviço (O.S.)**, contendo status, descrição, valor, data de emissão e data de conclusão.  
- Relacionar ordens de serviço com:  
  - **Serviços executados** (conserto, revisão, etc.).  
  - **Mecânicos responsáveis**.  
  - **Produtos utilizados**.  
- Controlar **estoque de produtos** disponíveis para os serviços.  
- Mapear **mão de obra** e seus valores associados.  

---

## 🗂️ Estrutura do Modelo
As principais entidades do modelo são:

- **Cliente**  
  - Dados pessoais e tipo de cliente (PF ou PJ).  
- **Veículo**  
  - Relacionado diretamente a um cliente.  
- **Ordem de Serviço (O.S.)**  
  - Associada a um cliente, contém status, datas e valor.  
- **Serviço**  
  - Relacionado a uma O.S., podendo ser **Conserto** ou **Revisão**.  
- **Produto**  
  - Associado a serviços e controlado via estoque.  
- **Mecânico**  
  - Pode estar vinculado a várias ordens de serviço.  
- **Estoque**  
  - Controla os produtos disponíveis.  

---

## 📊 Modelo Entidade-Relacionamento
O diagrama ER contempla:
- Relacionamento **1:N entre Cliente e Veículo**.  
- Relacionamento **1:N entre Cliente e O.S.**.  
- Relacionamento **N:N entre Ordem de Serviço e Mecânico**.  
- Relacionamento **N:N entre Produto e Estoque**.  
- Relacionamento **1:N entre O.S. e Serviços**.  
- Especialização de serviços em **Conserto** e **Revisão**.  

👉 Aqui está um exemplo de diagrama ER que pode ser incluído no repositório:

![Modelo ER da Oficina](./modelo-er-oficina.png)

---

## 🚀 Tecnologias e Ferramentas
- Modelagem: **MySQL Workbench**  
- Linguagem de definição: **SQL (DDL)**  
- Documentação: **Markdown (README.md)**  
