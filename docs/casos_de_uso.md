
# Diagrama de Casos de uso


| | |
| --- | --- |
| Projeto / Sistema: | Sistema de gerenciamento de orçamentos para MEIs |
| Cliente / Solicitante: | APS - Análise e projeto de sistema |
| Responsável(is): | Róger Campos |
| Data: | 05/11/26 |
| Versão: | 1.0 |

### 1 Sobre este documento

Este documento tem como objetivo organizar os casos de uso do sistema que serão detalhados posteriormente.

```mermaid
    usecase-beta
    %% atores
    actor cliente
    actor empreendedor
    %% actor bd ("SGBD")

    systemBoundary "Sistema MEI"

    solicitar_orcamento ("solicitar orçamento")
    emitir_orcamento ("emitir orçamento")
    cadastrar_empresa ("cadastrar empresa")

    manter_clientes ("manter clientes ")
    salvar_cliente ("salvar cliente")
    buscar_clientes ("buscar clientes")

    manter_servicos ("manter serviços")
    manter_materiais ("manter materiais")
    
    manter_fornecedores ("manter fornecedores")

    emitir_recibos ("emitir recibos")
    manter_recebimentos ("manter recebimentos")
    realizar_pagamento ("realizar pagamento")
    end

    %% cliente
    cliente -- solicitar_orcamento
    cliente -- realizar_pagamento

    %% empreendedor
    empreendedor -- emitir_recibos
    emitir_orcamento -- empreendedor
    empreendedor -- salvar_cliente
    empreendedor -- cadastrar_empresa
    empreendedor -- buscar_clientes

    %% sgbd

    %% Include e extend
    realizar_pagamento ..> : include emitir_recibos
    emitir_recibos ..> : include manter_recebimentos
    emitir_orcamento ..> : include manter_clientes
    salvar_cliente ..> : include manter_clientes

    manter_materiais ..> : extend emitir_orcamento
    emitir_orcamento ..> : extend solicitar_orcamento
    buscar_clientes ..> : extend emitir_orcamento
    emitir_orcamento ..> : extend manter_fornecedores
    emitir_orcamento ..> : extend manter_clientes
    emitir_orcamento ..> : extend manter_recebimentos
    emitir_orcamento ..> : extend manter_servicos
```
