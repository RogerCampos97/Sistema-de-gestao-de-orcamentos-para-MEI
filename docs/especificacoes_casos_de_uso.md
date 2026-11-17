# Especificação de Caso de Uso

Este documento contém as especificaçoes dos casos de uso do diagrama de casos de uso. Cada caso de uso está documentado separadamente e contém informações adicionais a respeito do mesmo.

| Especificacao de Caso de Uso | UC — 01 Cadastrar Empresa — Sistema MEI |
| --- | --- |
| caso de uso | UC-01 — Cadastrar Empresa |
| Ator principal | Empreendedor |
| Atores secundários | — |
| Resumo | Permite que o empreendedor cadastre sua empresa com cnpj, telefone e endereço, também é possivel, caso ele deseje, seus dados pessoais como seu telefone pessoal e nome. |
| Pré-condições | Empresa tenha cnpj válido e cpf seja também válido |
| Pós-condições | Empresa cadastrada e o programa já pode ser utilizado |
| **FLUXO PRINCIPAL** | |
| Fluxo principal | 1. Empreendedor informa o cnpj. <br> 2. O sistema verifica a validade do cnpj e automaticamente preenche os dados adicionais como razão social, endereço e telefone e email caso estejam disponíveis em api do gov. <br> 3. O Empreendedor pode editar os dados que desejar ou que estiverem incorretos / desatualizados. <br> 4. O empreendedor informa chave pix para pagamentos caso possua alguma. <br> 5.O sistema salva os dados após confirmação do empreendedor. |
| **FLUXOS ALTERNATIVOS** | |
| - FA01 — Empreendedor deseja disponibilizar dados pessoais| 1a. Empreendedor informa o cpf. <br> 2a. O sistema verifica a validade do cpf. <br> 2a. O empreendedor informa os dados adicionais que quiser disponibilizar (telefone, endereço, cpf). <br> 2a. Retorna ao passo 4. |
| **FLUXOS DE EXCECAO** | |
| FE01 — CNPJ informado inválido | 2a. O cnpj deve ser inserido novamente. <br> 2b. Retorna ao passo 2. |
| FE01 — CPF informado inválido | 2a. O cpf deve ser inserido novamente. <br> 2b. Retorna ao passo 2. |

| Especificacao de Caso de Uso | UC — 02 Manter catálogos — Sistema MEI |
| --- | --- |
| caso de uso | UC-02 — Manter catálogos |
| Ator principal | Empreendedor |
| Atores secundários | — |
| Resumo | Permite que o empreendedor manter catálogos de serviços, produtos e Fornecedores de materiais para fácil acesso aos mesmos quando preciso |
| Pré-condições | UC-01 empresa precisa estar cadastrada |
| Pós-condições | Item no catálogos de serviços, produtos e Fornecedores salvo e disponível para preenchimento em orçamentos e recibos. |
| **FLUXO PRINCIPAL** | |
| Fluxo principal | 1. O empreendedor informa o serviço a ser adicionado ao catálogo <br> 2. O sistema verifica se item com o mesmo nome existe <br> 3. O empreendedor preenche os dados do serviço: descrição, detalhes adicionais (se houver) e valor além da forma de cobrança (unidade, peso, metragem) <br> 3. O sistema salva os dados após confirmação do empreendedor. |
| **FLUXOS ALTERNATIVOS** | |
| - FA01 — O empreendedor deseja salvar um produto | 1a. O empreendedor seleciona a opção de produtos disponível como opção secundária na interface <br>  1b. o empreendedor preenche os dados do produto que desejar (descrição, marca, anexo de foto). <br> 1c. retorna ao passo 3.|
| - FA02 — O empreendedor deseja salvar um fornecedor | 1a. O empreendedor seleciona a opção de fornecedores disponível como opção secundária na interface <br>  1b. o empreendedor preenche os dados do fornecedor que desejar (cnpj, endereço, telefone, whatsapp, email), podendo informar primeiro o CNPJ e aguardar o preenchimento automático dos outros campos <br> 1c. retorna ao passo 3.|
| **FLUXOS DE EXCECAO** | |
| FE01 — CNPJ informado inválido em FA02 | 1c. O cnpj deve ser inserido novamente. <br> 1d. Retorna ao passo 1c de FA02. |

| Especificacao de Caso de Uso | UC - 03 |
| --- | --- |
| caso de uso | UC-01 — Marcar Consulta |
| Ator principal | |
| Atores secundários | |
| Resumo | |
| Pré-condições | |
| Pós-condições | |
| **FLUXO PRINCIPAL** | |
| Fluxo principal | |
| **FLUXOS ALTERNATIVOS** | |
| - FA01 — | |
| - FA02 — | |
| - FA03 — | |
| **FLUXOS DE EXCECAO** | |
| FE01 — | |

| Especificacao de Caso de Uso | UC - 04 |
| --- | --- |
| caso de uso | UC-01 — Marcar Consulta |
| Ator principal | |
| Atores secundários | |
| Resumo | |
| Pré-condições | |
| Pós-condições | |
| **FLUXO PRINCIPAL** | |
| Fluxo principal | |
| **FLUXOS ALTERNATIVOS** | |
| - FA01 — | |
| - FA02 — | |
| - FA03 — | |
| **FLUXOS DE EXCECAO** | |
| FE01 — | |

| Especificacao de Caso de Uso | UC - 05 |
| --- | --- |
| caso de uso | UC-01 — Marcar Consulta |
| Ator principal | |
| Atores secundários | |
| Resumo | |
| Pré-condições | |
| Pós-condições | |
| **FLUXO PRINCIPAL** | |
| Fluxo principal | |
| **FLUXOS ALTERNATIVOS** | |
| - FA01 — | |
| - FA02 — | |
| - FA03 — | |
| **FLUXOS DE EXCECAO** | |
| FE01 — | |