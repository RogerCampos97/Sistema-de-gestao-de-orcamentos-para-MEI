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

## 2. Requisitos Funcionais

| ID | Requisito | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- | --- |
| RF01 | Cadastrar o MEI | O sistema deve registrar Cnpj, nome fantasia, endereço e telefone | Alta | - |
| RF02 | Cadastrar o empreendedor | O sistema deve registrar nome, telefone etc. | Média | - |
| RF03 | Cadastrar Clientes | O sistema deve registrar nome, telefone, endereço | Alta | - |
| RF04 | Permitir a criação de orçamentos | O sistema deve registrar data, endereço (caso seja diferente do da casa do cliente), valor do serviço e descrição caso haja | Alta | RF01, RF03 |
| RF05 | Cadastrar lista de serviços no orçamento | Cada serviço do orçamento deve conter descrição individual do serviço realizado e preço individual | Alta | RF04 |
| RF06 | Gerar orçamento | O sistema deve gerar documento em PDF e/ou formato similar para impressão / compartilhamento com o preço totalizado | Alta | RF05 |
| RF07 | Exibir lista de clientes cadastrados | Mostrar lista de clientes | Média | RF03 |
| RF08 | Permitir buscar clientes | O sistema deve ter função de busca para o empreendedor poder buscar clientes em caso de necessidade | Média | RF07 |
| RF09 | Salvar dados de Fornecedores | O sistema deve registrar nome, telefone etc. de fornecedores de materiais / serviços | Baixa | - |
| RF10 | Emitir recibos | O sistema deve poder registrar valores recebidos por um orçamento e gerar um comprovante do recebimento de valores | Média | RF06 |
| RF11 | Permitir controle de recebimentos | o sistema deve ter tela para controle financeiro do empreendedor | Baixa | RF10 |
| RF12 | Permitir listar materiais no orçamento | O sistema deve permitir a listagem de custos referentes a materiais de um orçamento, com possibilidade de anexar comprovantes | Baixa | RF06 |

------

## 3. Requisitos Não Funcionais

| ID | Categoria | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- | --- |
| RNF01 | Usabilidade | A interface deve permitir criar um orçamento com facilidade | Alta | - |
| RNF02 | Segurança | O sistema deve permitir cadastro de senha para acesso ao sistema | Baixa | - |
| RNF03 | Desempenho | A realização de buscas de clientes/orçamentos devem retornar em menos de 2 segundos | Alta | - |
| RNF04 | Manutenibilidade | O Código deve ser organizado em camadas (MVC) com responsabilidades separadas | Alta | - |
| RNF05 | Persistência | Os dados devem ser armazenados em banco de dados para não serem perdidos ao encerrar o sistema | Alta | - |

## Clique [aqui](regras_de_negocio.md) para visualizar as Regras de negócio e os Requisitos Suplementares
