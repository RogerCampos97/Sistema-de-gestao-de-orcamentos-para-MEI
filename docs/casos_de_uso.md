
# Diagrama de Casos de uso

| | |
| --- | --- |
| Projeto / Sistema: | Sistema de gerenciamento de orçamentos para MEIs |
| Cliente / Solicitante: | APS - Análise e projeto de sistema |
| Responsável(is): | Róger Campos |
| Data: | 12/11/26 |
| Versão: | 1.0 |

## 1. Sobre este documento

Este documento tem como objetivo organizar os casos de uso do sistema que serão detalhados no documento de [especificações de casos de uso](docs/especificacoes_casos_de_uso.md).

## 2. Diagrama de casos de uso

```mermaid

usecase-beta
    %% atores
    actor cliente ("Cliente")
    actor empreendedor ("Empreendedor")

    systemBoundary "Sistema MEI"

    cadastrar_empresa ("cadastrar empresa")
    manter_clientes ("manter clientes")
    manter_catalogo ("manter catálogos")
    gerenciar_orcamento ("gerenciar orçamento")
    emitir_recibos ("emitir recibos")

    end

    %% cliente
    cliente -- gerenciar_orcamento
    %% cliente está interessado em receber o orçamento

    cliente -- emitir_recibos
    %% cliente está interessado em receber o recibo

    %% empreendedor
    empreendedor -- cadastrar_empresa
    empreendedor -- manter_clientes
    empreendedor -- manter_catalogo
    empreendedor -- gerenciar_orcamento 
    empreendedor -- emitir_recibos

    %% Include
    gerenciar_orcamento ..> :include manter_clientes
    %% obrigatório um orçamento ser relacionado a um cliente

    manter_catalogo ..> :extend gerenciar_orcamento 
    %% opcional manter o catálogo, um serviço pode ser feito sem ser adicionado ao catálogo, mesmo vale para um produto

    emitir_recibos ..> :include manter_clientes
    %% obrigatório um recibo ser relacionado a um cliente

```
