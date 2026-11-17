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

<br>
<br>
<br>

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

<br>
<br>
<br>

| Especificacao de Caso de Uso | UC — 03 Gerenciar orçamento — Sistema MEI |
| --- | --- |
| caso de uso | UC-03 — Gerenciar orçamento |
| Ator principal | Empreendedor |
| Atores secundários | Cliente |
| Resumo | Permite ao empreendedor criar orçamentos para seus clientes, e controlar quais serviços ou produtos estão nele e possibilita o compatilhamento do contato de fornecedores |
| Pré-condições | UC-01 empresa precisa estar cadastrada |
| Pós-condições | Orçamento deve estar criado e disponivel para o compartilhamento ou impressão |
| **FLUXO PRINCIPAL** | |
| Fluxo principal | 1. O empreendedor seleciona a opção de criar um orçamento <br> 2. são exibidas na tela opções para inserir um cliente cadastrado, inserir serviços, materiais, fornecedores e condições de pagamento, além de observações adicionais. <br> 3. O empreendedor escolhe por onde quer começar o orçamento, podendo iniciar por qualquer uma das opções. <br> 4. O sistema verifica se pelo menos um cliente e um serviço foram inseridos. <br> 5. O sistema gera o orçamento após confirmação dos dados, e exibe o mesmo. |
| **FLUXOS ALTERNATIVOS** | |
| - FA01 — O empreendedor deseja visualizar os orçamentos disponíveis | 1a. O empreendedor seleciona a opção de vizualizar os orçamentos na tela principal <br> 1b. O sistema exibe a lista dos orçamentos cadastrados, podendo ser modificada a ordem de classificação dos mesmos (data criação / modificação, valor), todas as ordens podem ser vistas de maneira invertida. |
| **FLUXOS DE EXCECAO** | |
| FE01 — O cliente não possui cadastro | 2a. O empreendedor seleciona a opção para criar um novo cliente disponível <br> 2b. o sistema direciona o usuário para o UC — 04, onde ele pode prosseguir com o cadastro, retornando para o passo 4 após a finalização. |
| FE03 — O empreendedor não deseja usar um serviço cadastrado | 3a. O empreendedor apenas informa os dados normalmente, de acodo com a UC — 02, mas não seleciona opção de cadastrar o serviço no catálogo. 3b. continua paa o passo 4. |

<br>
<br>
<br>

| Especificacao de Caso de Uso | UC — 04 — Manter clientes — Sistema MEI |
| --- | --- |
| caso de uso | UC-04 — Manter clientes |
| Ator principal | Empreendedor |
| Atores secundários | — |
| Resumo | Permite ao empreendedor manter cadastro dos clientes que ele possui |
| Pré-condições | UC-01 empresa precisa estar cadastrada |
| Pós-condições | Cliente cadastraado e disponível para seleção na criação de um orçamento e o mesmo pode ser vizualizado se necessário. |
| **FLUXO PRINCIPAL** | |
| Fluxo principal | 1. Empreendedor imforma CPF ou CNPJ do cliente <br> 2. O sistema verifica a validade dos mesmos e automaticamente preenche os dados disponíveis em api do gov <br> 3. O empreendedor edita os dados incorretos / desatualizados <br> 4. O sistema salva o cliente após confirmação dos dados. |
| **FLUXOS ALTERNATIVOS** | |
| - FA01 — O cliente já possui cadastro | 2a. O sistema informa ao empreendedor que o cadastro já existe <br> 2b. o sistema exibe o cadastro existente e deixa disponível opção para editá-lo |
| - FA02 — O empreendedor deseja vizualizar a lista de clientes | 1a. O empreendedor seleciona a opção de vizualizar os clientes na tela principal <br> 1b. O sistema exibe a lista dos clientes cadastrados, podendo ser modificada a ordem de classificação dos mesmos (alfabética, data da criação / modificação, intervalo de algum serviço realizado), todas as ordens podem ser vistas de maneira invertida. |
| - FA03 — O empreendedor deseja buscar um cliente | 1a. O empreendedor seleciona a opção de vizualizar os clientes na tela principal <br> 1b. O sistema exibe a lista dos clientes cadastrados <br> 1c. O empreendedor clica em opção de busca disponível na tela <br> 1d. O sistema realiza a busca por clientes em todos os campos buscáveis (nome, telefone, cpf, endereço) <br> 1e. O sistema exibe os resultados encontrados ou mensagem de erro caso não haja nenhum. |
| **FLUXOS DE EXCECAO** | |
| FE01 — CPF / CNPJ inválido | 3a. O sistema informa o erro no preenchimento dos dados e aguarda novo preenchimento. <br> 3b. retorna ao passo 1. |
| FE01 — CPF / CNPJ não informado | 3a. O sistema permite o preenchimento dos outros dados normalmente, apenas informando ao empreendeor a importância de possuir os dados corretos caso haja necessidade para cobranças ou processos no futuro. <br> 3b. retorna ao passo 3. |

<br>
<br>
<br>

| Especificacao de Caso de Uso | UC — 05 — Emitir recibos — Sistema MEI |
| --- | --- |
| caso de uso | UC-05 — Emitir recibos |
| Ator principal | Empreendedor |
| Atores secundários | Cliente |
| Resumo | Possibilita ao empreendedor gerar recibos de valores recebidos de um orçamento ou de serviços sem nenhum orçamento. |
| Pré-condições | UC-01 empresa precisa estar cadastrada |
| Pós-condições | Recibo está gerado e pronto para o compartilhamento ou impressão |
| **FLUXO PRINCIPAL** | |
| Fluxo principal | 1. Empreendedor seleciona qual orçamento o recibo é relacionado <br> 2. O empreendedor informa o valor recebido e adiciona uma descrição para o mesmo <br> 3. O empreendedor informa a forma de pagamento (pix, dinheiro, cartão de crédito, cartão de débito, boleto, cheque). <br> 4. O sistema gera o recibo correspondente.|
| **FLUXOS ALTERNATIVOS** | |
| —  | —  |
| **FLUXOS DE EXCECAO** | |
| FE01 — O orçamento não é informado | 1a. O sistema pede a inserção obrigatória de um cliente <br> 1b. O sistema prossegue normalmente para o passo 2. |
| FE02 — Valor informado é maior que o do orçamento | 2a. O sistema avisa e exibe opção para adicionar descrição de custos adicionais ou corrigir o erro <br> 2a.0. O sistema retorna ao  passo 2 se a opção de erro foi selecionada <br> 2a.1. O sistema exibe campo para adição descrição dos custos adicionais e prossegue para o passo 3.|
| FE03 — Valor informado é menor que o do orçamento | 2a. O sistema avisa e exibe opção para adicionar descrição de parcelamento / entrada ou corrigir o erro <br> 2b.0. O empreendedor informa a quantidade de parcelas caso selecione o parcelamento e prossegue para o passo 3. <br> 2b.1. O empreendedor informa os dados da entrada caso selecione a entrada e prossegue para o passo 3. <br> 2b.2. O sistema retorna para o passo 2 em caso de erro. |