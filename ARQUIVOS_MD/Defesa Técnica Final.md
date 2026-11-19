# UNIVERSIDADE CATÓLICA DE PERNAMBUCO
## GRADUAÇÃO EM CIÊNCIA DA COMPUTAÇÃO

**Integrantes:**
- Heitor José Gondim Brito
- João Gabriel Gomes de Sousa
- João Pedro Calaça Vasconcelos
- Vitor Araújo Pacheco de Miranda

# GREENMIFY
## Defesa Técnica Final

**Disciplina:** Processos e Requisitos de Software  
**Professora:** Ivna Cristine Brasileiro Valença  
**Recife — 2026**

---

# 1. Apresentação do projeto

O Greenmify é um marketplace digital voltado ao setor agrícola. Seu objetivo é conectar produtores rurais e consumidores em uma plataforma para divulgação, pesquisa e comercialização de produtos e equipamentos agrícolas.

A proposta surgiu da identificação de dificuldades enfrentadas pelos produtores para divulgar seus produtos e pelos consumidores para encontrar opções, comparar informações e conhecer os vendedores.

# 2. Problema e solução proposta

## Problemas identificados

- Dificuldade dos produtores em divulgar seus produtos.
- Dificuldade dos consumidores em encontrar produtos agrícolas.
- Informações espalhadas em diferentes canais.
- Dificuldade de conhecer os produtores e seus produtos.
- Falta de uma plataforma centralizada para essa interação.

## Solução proposta

O Greenmify reúne em uma única plataforma funcionalidades de cadastro e gerenciamento de produtos, pesquisa e filtros, visualização de informações, comunicação entre consumidores e produtores e moderação de anúncios.

# 3. Product Backlog e requisitos

O Product Backlog inicial foi organizado em **20 histórias de usuário**, distribuídas em **seis épicos**. A priorização foi realizada utilizando a técnica **MoSCoW**, que classifica as funcionalidades conforme sua importância.

| Épico | Funcionalidade |
|---|---|
| E01 | Busca e descoberta de produtos |
| E02 | Visualização e informações dos produtos |
| E03 | Cadastro e gerenciamento de produtos |
| E04 | Comunicação entre consumidor e vendedor |
| E05 | Gerenciamento de usuários e perfis |
| E06 | Moderação e segurança |

As histórias classificadas como **Must** foram consideradas essenciais para o funcionamento do marketplace. As classificadas como **Should** representam funcionalidades importantes, enquanto as **Could** são recursos desejáveis que podem agregar valor ao produto.

# 4. Evolução das Sprints

O desenvolvimento foi organizado em seis Sprints, agrupadas por épicos:

| Sprint | Épico | Funcionalidades desenvolvidas | Story Points |
|---|---|---|---:|
| 1 | E03 | Cadastro e gerenciamento de produtos | 45 |
| 2 | E01 | Busca, filtros e favoritos | 16 |
| 3 | E02 | Visualização de produtos e produtores | 18 |
| 4 | E04 | Comunicação entre consumidor e vendedor | 18 |
| 5 | E05 | Gerenciamento de usuários e perfis | 18 |
| 6 | E06 | Moderação e segurança | 20 |
| **Total** | | | **135** |

A divisão permitiu desenvolver o produto de maneira incremental, concentrando cada Sprint em um conjunto de funcionalidades relacionadas.

# 5. Decisões de requisitos: BUG01 e MUD01

Durante o desenvolvimento da Sprint 1, foi identificado o **BUG01**, relacionado ao cadastro de produtos agrícolas e equipamentos, nas histórias US07 e US08.

A partir desse problema, foi registrada a **MUD01 — Unificação do cadastro e adição de unidade de medida**.

A mudança propôs:

- Unificar o processo de cadastro de produtos e equipamentos.
- Manter os campos específicos de cada tipo.
- Adicionar o campo “Unidade de medida” ao cadastro de produtos, com opções como kg, unidade, caixa, litro ou tonelada.
- Atualizar os critérios de aceitação.
- Corrigir o BUG01.

A equipe aceitou a mudança por sua relação direta com o épico E03 e por melhorar a organização e a quantidade de informações disponíveis no cadastro.

As histórias US07 e US08 foram mantidas no backlog para preservar o histórico e a rastreabilidade da alteração. Conforme o relatório final de métricas, o BUG01 foi corrigido e a MUD01 foi implementada.

# 6. Requisitos não funcionais

Além das funcionalidades, foram definidos sete requisitos não funcionais para orientar a qualidade do Greenmify:

| ID | Requisito não funcional | Objetivo |
|---|---|---|
| RNF-01 | Desempenho nas buscas | Retornar resultados em até 2 segundos nas condições de teste definidas. |
| RNF-02 | Otimização de imagens | Compactar e otimizar imagens durante o envio. |
| RNF-03 | Controle de acesso por perfil | Restringir funcionalidades conforme as permissões de cada perfil. |
| RNF-04 | Proteção de dados pessoais | Proteger dados pessoais por criptografia e controles de acesso. |
| RNF-05 | Funcionamento em conexões instáveis | Permitir acesso offline parcial e sincronização quando a conexão retornar. |
| RNF-06 | Confiabilidade e integridade dos dados | Evitar perdas, inconsistências e duplicações indevidas. |
| RNF-07 | Clareza das mensagens de erro | Orientar o usuário com mensagens simples e claras. |

Esses requisitos consideram aspectos de desempenho, eficiência, segurança, privacidade, disponibilidade, confiabilidade e usabilidade.

# 7. Arquitetura e decisões arquiteturais

As decisões arquiteturais foram relacionadas aos requisitos não funcionais, indicando estratégias técnicas para atendê-los.

| Decisão | Estratégia | RNF relacionado |
|---|---|---|
| DA-01 | Otimizar consultas ao banco de dados e avaliar índices e paginação. | RNF-01 |
| DA-02 | Processar imagens no upload, validando formato e tamanho. | RNF-02 |
| DA-03 | Implementar autenticação e autorização por perfil no servidor. | RNF-03 |
| DA-04 | Adotar criptografia em repouso e em trânsito e gerenciar chaves com segurança. | RNF-04 |
| DA-05 | Definir armazenamento local, funcionalidades offline e sincronização. | RNF-05 |
| DA-06 | Utilizar transações e validações para preservar a integridade dos dados. | RNF-06 |
| DA-07 | Padronizar o tratamento de erros e as mensagens exibidas na interface. | RNF-07 |

As decisões mostram como os requisitos de qualidade influenciam a estrutura e o comportamento técnico esperado do sistema. Elas representam as estratégias arquiteturais documentadas pelo grupo.

# 8. Métricas e desempenho do processo

Para analisar o processo de desenvolvimento, foram utilizadas as métricas de Story Points planejados e concluídos, velocity, percentual de conclusão e Burndown.

## 8.1 Resultado geral

| Indicador | Resultado |
|---|---:|
| Sprints realizadas | 6 |
| Histórias de usuário | 20 |
| Story Points planejados | 135 |
| Story Points concluídos | 135 |
| Percentual de conclusão | 100% |
| Velocity média | 22,5 Story Points |

## 8.2 Velocity por Sprint

| Sprint | Planejado | Concluído | Velocity | Conclusão |
|---|---:|---:|---:|---:|
| 1 | 45 | 45 | 45 | 100% |
| 2 | 16 | 16 | 16 | 100% |
| 3 | 18 | 18 | 18 | 100% |
| 4 | 18 | 18 | 18 | 100% |
| 5 | 18 | 18 | 18 | 100% |
| 6 | 20 | 20 | 20 | 100% |
| **Total** | **135** | **135** | **135** | **100%** |

A Sprint 1 apresentou a maior velocity, com 45 pontos. Nas demais Sprints, a quantidade concluída variou entre 16 e 20 pontos. A comparação deve considerar a quantidade e a complexidade das histórias selecionadas em cada ciclo.

## 8.3 Burndown

Os gráficos de Burndown foram utilizados para representar a redução dos pontos restantes conforme as histórias eram concluídas. Nas seis Sprints, o trabalho planejado chegou a zero ao final de cada ciclo.

Os gráficos do relatório foram construídos com base nos pontos restantes após a conclusão de cada história. Portanto, representam a evolução por etapas, e não registros diários de acompanhamento.

# 9. Gargalos e melhorias no processo

A análise das Sprints e das retrospectivas permitiu identificar pontos que poderiam ser melhorados:

- **Comunicação:** necessidade de realizar acompanhamentos mais frequentes entre os integrantes.
- **Divisão das atividades:** necessidade de distribuir melhor as tarefas, considerando sua complexidade e a disponibilidade dos membros.
- **Testes:** necessidade de reservar tempo suficiente para testar as funcionalidades.
- **Cadastro:** o BUG01 evidenciou a necessidade de revisar o processo de cadastro, o que levou ao registro da MUD01.

Como melhorias, a equipe definiu acompanhamentos mais frequentes, melhor distribuição das atividades e utilização contínua do GitHub Projects para visualizar tarefas nos estados To Do, Doing e Done.

# 10. Resultados e conclusão

Ao longo do projeto, foram organizadas e consideradas concluídas 20 histórias de usuário, distribuídas em seis Sprints, totalizando 135 Story Points.

O grupo também identificou e tratou um problema no cadastro, registrou uma mudança de requisito, atualizou o backlog e manteve a rastreabilidade entre as histórias originais e a alteração.

A definição dos requisitos não funcionais e das decisões arquiteturais permitiu relacionar as necessidades de qualidade às estratégias técnicas previstas para o sistema.

O desenvolvimento do Greenmify demonstrou a importância do planejamento incremental, da priorização dos requisitos, do acompanhamento por métricas e da capacidade de adaptar o produto quando problemas ou novas necessidades são identificados.

**Concluímos que o projeto permitiu aplicar conceitos de engenharia de software e compreender a relação entre requisitos, arquitetura e processo de desenvolvimento.**
