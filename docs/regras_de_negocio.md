# Regras de Negócio e Requisitos Suplementares

## 1. Sobre este documento

Este documento tem como objetivo organizar as regras de negócio e requisitos suplementares do programa para servir de referência para as proximas etapas do projeto.

## 2. Regras de Negócio

| ID | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- |
| RN1 | O sistema não deve permitir clientes duplicados | Alta | RF03 |
| RN2 | O sistema deve permitir a emisão de recibos mesmo que não hajam orçamentos correspondentes | Alta | RF04, RF10 |
| RN3 | O sistema não deve permitir orçamentos sem que o mesmo esteja atrelado a um cliente cadastrado | Alta | RF03, RF06 |
| RN4 | Recebimentos de valores devem sempre possuir um cliente | Alta | RF03 |

## 3. Requisitos Suplementares

| ID | Categoria | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- | --- |
| RS1 | Segurança | O sistema deve armazenar os dados com  segurança, seguindo a LGPD | Alta | RF01, RF03 |
| RS2 | Manutenção | O codigo deve ser organizado e bem documentado | Alta | - |
| RS3 | Usabilidade | O sistema deve possuir menus intuitivos e textos de ajuda para que o usuário não tenha dificuldades no manuseio | Alta | - |
| RS4 | O sistema deve ter uma interface disponível em mais de um idioma | Média | - | - |
