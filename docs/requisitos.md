# Documento de Especificação de Requisitos

| | |
| --- | --- |
| Projeto / Sistema: | Sistema de gerenciamento de orçamentos para MEIs |
| Cliente / Solicitante: | APS - Análise e projeto de sistema |
| Responsável(is): | Róger Campos |
| Data: | 05/11/26 |
| Versão: | 1.0 |

## 1. Introdução

### 1.1 Sobre este documento

Este documento tem como objetivo organizar os requisitos funcionais e não funcionais do programa para servir de referência para as proximas etapas do projeto.

### 1.2 Descrição do Mini-Mundo

Os MEIs (Micro empreendedores individuais) já contam com várias alternativas para a geracão de orçamentos e o controle do portfólio de clientes, mas estes ou não são muito intuitivos, ou exigem pagamento para funções essenciais. Os principais envolvidos são os próprios MEIs e seus clientes, é necessário que ambos sejam cadastrados para que um orçamento possa ser gerado, por isso é importante que os requisitos e as regras de negócio sejam cumpridos(as).

### 1.3 Propósito do Sistema

O propósito é criar um sistema simples, fácil de usar, e sem custos extras para que os Micro empreendedores tenham uma forma mais simples e rápida, sem preçisar pagar por funções básicas, para gerar orçamentos para entregar para os seus clientes, e também uma plataforma para salvar os dados desses mesmos clientes.

## 2. Requisitos Funcionais

| ID | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- |
| RF01 | O sistema deve realizar o cadastro do MEI, registrando o Cnpj, nome fantasia, endereço e telefone, além de registrar o nome do empreendedor e seu telefone pessoal | Alta | - |
| RF02 | O sistema deve permitir cadastrar os Clientes registrando o nome, telefone, endereço | Alta | - |
| RF03 | O sistema deve permitir a criação de orçamentos, registrando a data, endereço (caso seja diferente do da casa do cliente), valor do serviço e descrição adicional, caso haja | Alta | RF01, RF03 |
| RF04 | O sistema deve cadastrar a lista de serviços no orçamento, cada entrada deve conter: descrição individual do serviço realizado, preço individual e quantidade | Alta | RF04 |
| RF05 | O sistema deve gerar orçamento, este deve ser documento em PDF e/ou formato similar para impressão / compartilhamento com o preço dos serviços totalizado | Alta | RF05 |
| RF06 | O sistema deve exibir a lista de clientes cadastrados para o empreendedor, exibindo nome e permitir que seja aberta nova interface para vizualizar todos os dados do cliente | Média | RF03 |
| RF07 | O sistema deve permitir que o empreendedor possa buscar clientes em caso de necessidade | Média | RF07 |
| RF08 | O sistema deve permitir registrar dados de fornecedores com nome e telefone dos mesmos | Baixa | - |
| RF9 | O sistema deve emitir recibos, podendo registrar valores recebidos por um orçamento e gerar um comprovante do recebimento destes valores que possa ser compartilhado / impresso para entrega ao cliente | Média | RF06 |
| RF10 | O sistema deve Permitir controle de recebimentos, essa tela deve conter dados para o controle financeiro do empreendedor, tendo os valores recebidos, custos de produção e lucro obtido em cada serviço e em período semanal / mensal | Baixa | RF10 |
| RF11 | O sistema deve permitir listar materiais no orçamento, essa listagem deve fornecer a possibilidade de anexar uma imagem / documento de um comprovante | Baixa | RF06 |

------

## 3. Requisitos Não Funcionais

| ID | Categoria | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- | --- |
| RNF01 | Usabilidade | A interface deve permitir criar um orçamento com facilidade | Alta | - |
| RNF02 | Segurança | O empreendedor deve ter a possibilidade de utilizar uma senha para acesso ao sistema | Baixa | - |
| RNF03 | Desempenho | A realização de buscas de clientes/orçamentos devem retornar em menos de 2 segundos | Alta | - |
| RNF04 | Manutenibilidade | O Código deve ser organizado em camadas (MVC) com responsabilidades separadas | Alta | - |
| RNF05 | Persistência | Os dados devem ser armazenados em banco de dados para não serem perdidos ao encerrar o sistema | Alta | - |

## Clique [aqui](regras_de_negocio.md) para visualizar as Regras de negócio e os Requisitos Suplementares
