
# Diagrama de Casos de uso

```mermaid
    usecase-beta
    %% atores
    actor cl("Cliente")
    actor empreendedor
    %% actor bd ("SGBD")

    systemBoundary "Sistema MEI"

    solicitar_orcamento ("solicitar orçamento")
    emitir_orcamento ("emitir orçamento")
    cadastrar_empresa ("cadastrar empresa")

    cadastrar_cliente ("cadastrar cliente")
    manter_clientes ("manter clientes ")
    salvar_cliente ("salvar cliente")
    buscar_clientes ("buscar clientes")

    ms ("manter serviços")
    manter_materiais ("manter materiais")
    
    cf ("cadastrar fornecedores")
    mf ("manter fornecedores")

    emitir_recibos ("emitir recibos")
    manter_recebimentos ("manter recebimentos")
    rp ("realizar pagamento")
    end

    %% cliente
    cl -- solicitar_orcamento
    cl -- rp

    %% empreendedor
    empreendedor -- emitir_recibos
    emitir_orcamento -- empreendedor
    empreendedor -- salvar_cliente
    empreendedor -- cadastrar_empresa
    empreendedor -- cf
    empreendedor -- buscar_clientes

    %% sgbd

    %% Include e extend
    rp ..> : include emitir_recibos
    emitir_recibos ..> : include manter_recebimentos
    emitir_orcamento ..> : include cadastrar_cliente
    salvar_cliente ..> : include cadastrar_cliente

    manter_materiais ..> : extend emitir_orcamento
    emitir_orcamento ..> : extend solicitar_orcamento
    buscar_clientes ..> : extend emitir_orcamento
```
