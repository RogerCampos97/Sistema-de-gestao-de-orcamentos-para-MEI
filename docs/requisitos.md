# Documento de Especificação de Requisitos
| | |
| --- | --- |
| Projeto / Sistema: | Sistema de gerenciamento de orçamentos para MEIs |
| Cliente / Solicitante: | APS - Análise e projeto de sistema |
| Responsável(is): | Róger Campos |
| Data:| 05/11/26 |
| Versão: | 1.0 |

## 1. Introdução
### 1.1 Sobre este documento

Este documento tem como objetivo organizar os requisitos funcionais e não funcionais do programa para servir de referência para as proximas etapas do projeto.

### 1.2 Descrição do Mini-Mundo

Os MEIs (Micro empreendedores individuais) já contam com várias alternativas para a geracão de orçamentos e o controle do portfólio de clientes, mas estes ou não são muito intuitivos, ou exigem pagamento para funções essenciais. Os principais envolvidos são os próprios MEIs e seus clientes, é necessário que ambos sejam cadastrados para que um orçamento possa ser gerado, por isso é importante que os requisitos e as regras de negócio sejam cumpridos(as).

### 1.3 Propósito do Sistema

O propósito é criar um sistema simples, fácil de usar, e sem custos extras para que os Micro empreendedores tenham uma forma mais simples e rápida, sem preçisar pagar por funções básicas, para gerar orçamentos para entregar para os seus clientes, e também uma plataforma para salvar os dados desses mesmos clientes.

## Requisitos Funcionais

| ID | Requisito | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- | --- |
| RF01 | Cadastrar o MEI | Registrar Cnpj, nome fantasia, endereço e telefone | Alta | - |
| RF02 | Cadastrar o empreendedor | Registrar nome, telefone etc. | Média | - |
| RF03 | Cadastrar Clientes | Registrar nome, telefone, endereço | Alta | - |
| RF04 | Permitir a criação de orçamentos | Registrar data, endereço (caso seja diferente do da casa do cliente), valor do serviço e descrição caso haja | Alta | RF01, RF03 |
| RF05 | Cadastrar lista de serviços | Descrição individual, no orçamento de cada serviço a ser realizado com preço individual | Alta | RF04 |
| RF06 | Gerar orçamento | Gerar documento em PDF e/ou formato similar para impressão / compartilhamento | Alta | RF05 |
| RF07 | Exibir lista de clientes cadastrados | Mostrar lista de clientes | Média | RF03 |
| RF08 | Permitir buscar clientes | Ter função de busca para o empreendedor poder buscas em caso de necessidade | Média | RF07 |
| RF09 | Salvar dados de Fornecedores | Registrar nome, telefone etc. de fornecedores de materiais / serviços | Baixa | - |
| RF10 | Emitir recibos | Registrar valores recebidos por um orçamento ou valores recebidos sem nenhum orçamento e gerar recibos em PDF ou formato similar | Média | RF06 |
| RF11 | Permitir controle de recebimentos | Ter tela para controle financeiro do empreendedor | Baixa | RF10 |
| RF12 | Permitir listar materiais no orçamento | Permitir a listagem de custos referentes a materiais de um orçamento, com possibilidade de anexar comprovantes  | Baixa | RF06 |
---

## Requisitos Não Funcionais

| ID | Categoria | Descrição | Prioridade | Depende de |
| --- | --- | --- | ---| --- |
| RNF01 | Usabilidade | A interface deve permitir criar um orçamento com facilidade | Alta | - |
| RNF02 | Segurança | Permitir cadastro de senha para acesso ao sistema  | Baixa | - |
| RNF03 | Desempenho | Buscas de clientes/orçamentos devem retornar em menos de 2 segundos | Alta | - |


