# UNIVERSIDADE CATÓLICA DE PERNAMBUCO

## GRADUAÇÃO EM CIÊNCIA DA COMPUTAÇÃO

Heitor José Gondim Brito  
João Gabriel Gomes de Sousa  
João Pedro Calaça Vasconcelos  
Vitor Araújo Pacheco de Miranda

# GREENMIFY
## Gestão de Mudança

**Recife**  
**2026**

---

# Greenmify: Gestão de Mudança

**Trabalho apresentado à disciplina de Processos e Requisitos de Software**, do curso de Ciência da Computação da Universidade Católica de Pernambuco, como requisito para avaliação da disciplina.

**Professora:** Ivna Cristine Brasileiro Valença

**Recife — 2026**

---

## 1. Objetivo

Demonstrar a capacidade do grupo de gerenciar uma mudança de requisito durante o desenvolvimento, analisando seus impactos, atualizando o backlog e mantendo a rastreabilidade entre o requisito original e a alteração. A mudança será implementada na próxima sprint, sem alterar os resultados da Sprint 1.

## 2. Requisito Original

**US07 – Cadastrar produtos agrícolas / US08 – Cadastrar equipamentos agrícolas**

- **US07:** Como produtor, quero cadastrar meus produtos agrícolas para disponibilizá-los na plataforma.
- **US08:** Como produtor, quero cadastrar meus equipamentos agrícolas para disponibilizá-los na plataforma.
- **Épico:** E03 – Cadastro e Gerenciamento de Produtos
- **Story Points:** 20 (US07) e 20 (US08)
- **Origem:** Sprint 1

### Critérios de aceitação originais

- O produtor deve conseguir cadastrar um produto.
- O produtor deve conseguir cadastrar um equipamento agrícola.
- O sistema deve solicitar os dados principais de cada cadastro.
- O sistema deve validar os campos obrigatórios.
- O item deve ser armazenado após o cadastro.

## 3. Mudança solicitada

**MUD01 – Unificação do cadastro e adição de unidade de medida**

Unificar as funcionalidades de cadastro de produtos e equipamentos agrícolas em um único processo de cadastro, mantendo os campos específicos de cada tipo. Além disso, será adicionado o campo “Unidade de medida” ao cadastro de produtos agrícolas, permitindo informar como o produto é comercializado ou quantificado, como kg, unidade, caixa, litro ou tonelada.

## 4. Motivo da mudança

A mudança foi solicitada após a identificação do BUG01, que afeta o cadastro de produtos e equipamentos. Como os dois cadastros apresentam um problema relacionado, decidiu-se unificar o processo para tratar as funcionalidades de forma conjunta. A inclusão da Unidade de medida também permitirá que o produtor informe de forma mais completa como o produto é comercializado ou quantificado.

## 5. Análise do impacto

A mudança afeta as histórias US07 e US08. Será necessário ajustar a interface para utilizar um único fluxo de cadastro, mantendo os campos específicos para produtos e equipamentos. No caso de produtos, será incluído o campo Unidade de medida. Também serão necessários ajustes no banco de dados, backend e testes. O BUG01 deverá ser corrigido durante a implementação da mudança.

## 6. Decisão do grupo

**Decisão: Aceitar.**

A mudança está diretamente relacionada ao épico E03, permite tratar conjuntamente o problema identificado no BUG01 e acrescenta uma informação importante ao cadastro de produtos.

## 7. Backlog atualizado

As histórias US07 e US08 permanecem registradas no backlog para preservar o histórico e a rastreabilidade, porém passam a estar relacionadas à MUD01.

## 8. Critérios de aceitação atualizados

- O produtor consegue cadastrar um produto agrícola.
- O produtor consegue cadastrar um equipamento agrícola.
- O sistema identifica o tipo de cadastro realizado.
- O sistema apresenta os campos específicos de cada tipo.
- O cadastro de produtos possui o campo Unidade de medida.
- A unidade de medida é armazenada corretamente.
- O sistema valida os campos obrigatórios.
- O BUG01 foi corrigido.
- O cadastro é finalizado corretamente.

## 9. Rastreabilidade da mudança

- **Épico:** E03 – Cadastro e gerenciamento de produtos.
- **Histórias:** US07 – Cadastrar produtos agrícolas e US08 – Cadastrar equipamentos agrícolas.
- **Problema identificado:** BUG01 – Erro no cadastro de produtos e equipamentos.
- **Mudança:** MUD01 – Unificação do cadastro e adição de unidade de medida.
- **Implementação:** Próxima Sprint.

## 10. Registro da mudança

A MUD01 foi registrada no GitHub como uma mudança de requisito, relacionada às histórias US07 e US08 e ao BUG01.

- **Status:** To Do.
- **Implementação:** Próxima Sprint.
- **Épico:** E03 – Cadastro e gerenciamento de produtos.

## 11. Alterações realizadas no backlog

- Unificação do processo de cadastro de produtos e equipamentos.
- Manutenção dos campos específicos de cada tipo.
- Inclusão do campo Unidade de medida no cadastro de produtos.
- Atualização dos critérios de aceitação.
- Relacionamento da mudança com o BUG01.
- Manutenção das histórias US07 e US08 para preservar a rastreabilidade.

## 12. Resumo

A MUD01 altera o processo de cadastro de produtos e equipamentos, unificando as funcionalidades e adicionando a Unidade de medida aos produtos agrícolas. A mudança está relacionada ao BUG01 e será implementada na próxima Sprint juntamente com sua correção.
