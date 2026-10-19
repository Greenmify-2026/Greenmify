# Greenmify — Requisitos Não Funcionais

## Integrantes do grupo

- João Pedro Calaça Vasconcelos
- João Gabriel Gomes de Sousa
- Victor Araújo Pacheco de Miranda
- Heitor José Gondim Brito
 
## 1. Introdução

O Greenmify é um marketplace agrícola que conecta produtores rurais e consumidores, permitindo a divulgação, pesquisa e comparação de produtos, além da comunicação entre usuários.

Este documento apresenta os requisitos não funcionais (RNFs) do projeto, suas classificações, justificativas, critérios de aceitação e relações com as histórias de usuário. Também demonstra como esses requisitos influenciam as decisões arquiteturais e as soluções técnicas propostas.

## 2. Requisitos Não Funcionais

### RNF-01 — Desempenho nas buscas

**Descrição:** As buscas de produtos devem retornar resultados em até 2 segundos, nas condições de teste definidas pela equipe.

**Classificação:** Desempenho.

**Justificativa:** Permitir que os consumidores encontrem produtos rapidamente, proporcionando uma experiência de navegação eficiente.

**Critérios de aceitação:**
- As buscas devem retornar resultados em até 2 segundos nas condições de teste acordadas.
- Os testes devem incluir pesquisas por nome e aplicação dos filtros disponíveis.
- O tempo de resposta deve ser medido por testes de desempenho.

**Histórias relacionadas:** US01 — Pesquisar produtos agrícolas; US02 — Filtrar produtos; US03 — Favoritar produtos; US04 — Visualizar informações do produto; US06 — Comparar produtos.

**Decisão arquitetural — DA-01:** Otimizar consultas ao banco de dados e avaliar o uso de índices e paginação.

**Justificativa da decisão:** Consultas eficientes e carregamento paginado reduzem o volume de dados processados e podem diminuir o tempo de resposta.

### RNF-02 — Otimização de imagens

**Descrição:** As imagens dos produtos devem ser compactadas e otimizadas automaticamente durante o envio, mantendo qualidade visual adequada para identificar os produtos.

**Classificação:** Desempenho e eficiência no uso de recursos.

**Justificativa:** Reduzir o consumo de armazenamento e de dados móveis, além de melhorar o carregamento das páginas.

**Critérios de aceitação:**
- As imagens aceitas devem ser otimizadas automaticamente durante o upload.
- A qualidade visual deve permanecer suficiente para identificar o produto.
- O sistema deve informar falhas no envio ou no processamento.
- A imagem não deve ser apresentada como publicada antes da conclusão do processo.

**Histórias relacionadas:** US07 — Cadastrar produtos agrícolas; US08 — Cadastrar equipamentos agrícolas; US09 — Editar produtos.

**Decisão arquitetural — DA-02:** Implementar processamento de imagens no fluxo de upload, com validação de formato e tamanho e armazenamento da versão otimizada.

**Justificativa da decisão:** O processamento automático padroniza as imagens e reduz o uso de recursos sem exigir ações adicionais do usuário.

### RNF-03 — Controle de acesso por perfil

**Descrição:** O sistema deve restringir funcionalidades e dados conforme as permissões dos perfis de comprador, vendedor e administrador.

**Classificação:** Segurança.

**Justificativa:** Impedir acessos indevidos e garantir que cada usuário execute apenas as ações autorizadas.

**Critérios de aceitação:**
- Cada perfil deve acessar somente as funcionalidades autorizadas.
- Compradores não devem executar ações exclusivas de vendedores ou administradores.
- Vendedores devem gerenciar apenas os produtos sob sua responsabilidade.
- A aprovação e a remoção de anúncios devem ser restritas aos usuários autorizados.
- Tentativas de acesso não autorizado devem ser bloqueadas no servidor.

**Histórias relacionadas:** US07 — Cadastrar produtos agrícolas; US08 — Cadastrar equipamentos agrícolas; US09 — Editar produtos; US10 — Alterar disponibilidade dos produtos; US14 — Criar uma conta; US15 — Editar dados do perfil; US16 — Completar perfil de produtor; US17 — Visualizar anúncios; US18 — Aprovar ou reprovar anúncios; US19 — Denunciar anúncios inadequados; US20 — Remover anúncios inadequados.

**Decisão arquitetural — DA-03:** Implementar autenticação e autorização por perfil no servidor.

**Justificativa da decisão:** A validação no servidor protege os dados e as operações mesmo quando alguém tenta contornar as restrições da interface.

### RNF-04 — Proteção de dados pessoais

**Descrição:** Dados pessoais, como CPF e endereço, devem ser protegidos por criptografia e controles de acesso adequados.

**Classificação:** Segurança e privacidade.

**Justificativa:** Reduzir o risco de exposição indevida de informações de compradores e produtores e respeitar a legislação aplicável, incluindo a LGPD.

**Critérios de aceitação:**
- Os dados definidos como sensíveis devem ser protegidos durante o armazenamento.
- A transmissão de dados pessoais deve utilizar comunicação protegida por TLS.
- O acesso aos dados deve ser limitado a operações e usuários autorizados.
- As chaves criptográficas devem ser armazenadas e gerenciadas separadamente dos dados protegidos.
- O tratamento dos dados deve respeitar a legislação aplicável.

**Histórias relacionadas:** US11 — Entrar em contato com o produtor; US12 — Receber mensagens; US13 — Visualizar conversas; US14 — Criar uma conta; US15 — Editar dados do perfil; US16 — Completar perfil de produtor.

**Decisão arquitetural — DA-04:** Adotar criptografia em repouso e em trânsito, gerenciamento seguro de chaves e controle de acesso aos dados pessoais.

**Justificativa da decisão:** Esses mecanismos reduzem o risco de exposição durante o armazenamento, a transmissão e o acesso às informações. A equipe deve definir quais campos exigem criptografia reversível e quais podem utilizar outras técnicas de proteção.

### RNF-05 — Funcionamento em conexões instáveis

**Descrição:** O sistema deve oferecer suporte a conexões instáveis, permitindo acesso offline parcial e retomada das operações compatíveis após o restabelecimento da conexão.

**Classificação:** Disponibilidade e tolerância a falhas de conectividade.

**Justificativa:** Facilitar o uso do Greenmify por produtores rurais em regiões com acesso limitado à internet.

**Critérios de aceitação:**
- O sistema deve informar quando a conexão estiver indisponível.
- Informações previamente armazenadas e autorizadas devem continuar acessíveis offline quando previsto.
- Operações que dependam do servidor devem indicar quando não puderem ser concluídas.
- As operações compatíveis devem poder ser retomadas ou sincronizadas após o restabelecimento da conexão.
- A sincronização deve tratar conflitos e evitar duplicações.
- As funcionalidades disponíveis offline devem ser definidas pela equipe.

**Histórias relacionadas:** US01 — Pesquisar produtos agrícolas; US02 — Filtrar produtos; US04 — Visualizar informações do produto; US05 — Visualizar perfil do produtor; US07 — Cadastrar produtos agrícolas; US09 — Editar produtos; US10 — Alterar disponibilidade dos produtos; US11 — Entrar em contato com o produtor; US12 — Receber mensagens; US13 — Visualizar conversas; US15 — Editar dados do perfil; US16 — Completar perfil de produtor.

**Decisão arquitetural — DA-05:** Definir armazenamento local, funcionalidades offline e mecanismos de sincronização com o servidor.

**Justificativa da decisão:** O armazenamento local permite consultar informações disponíveis sem conexão, enquanto a sincronização recupera as alterações pendentes. Operações que dependam de confirmação do servidor não devem ser apresentadas como concluídas antes dessa confirmação.

### RNF-06 — Confiabilidade e integridade dos dados

**Descrição:** O sistema deve tratar falhas durante operações críticas, preservando a consistência dos dados e evitando perdas ou duplicações indevidas.

**Classificação:** Confiabilidade e integridade.

**Justificativa:** Proteger informações de produtos, disponibilidade, contas, mensagens e demais operações importantes para o marketplace.

**Critérios de aceitação:**
- As operações críticas devem preservar a consistência dos dados.
- Falhas não devem deixar operações parcialmente confirmadas sem tratamento definido.
- Solicitações repetidas devem ser tratadas para evitar duplicações quando aplicável.
- O sistema deve informar quando uma operação não puder ser concluída.
- Devem existir mecanismos adequados de recuperação e registro de falhas.

**Histórias relacionadas:** US03 — Favoritar produtos; US07 — Cadastrar produtos agrícolas; US08 — Cadastrar equipamentos agrícolas; US09 — Editar produtos; US10 — Alterar disponibilidade dos produtos; US11 — Entrar em contato com o produtor; US12 — Receber mensagens; US13 — Visualizar conversas; US14 — Criar uma conta; US15 — Editar dados do perfil; US16 — Completar perfil de produtor; US18 — Aprovar ou reprovar anúncios; US19 — Denunciar anúncios inadequados; US20 — Remover anúncios inadequados.

**Decisão arquitetural — DA-06:** Utilizar transações de banco de dados, validações de integridade e mecanismos de recuperação e idempotência nas operações críticas.

**Justificativa da decisão:** Esses mecanismos ajudam a impedir registros inconsistentes, tratar falhas e evitar que a repetição de uma solicitação execute a mesma operação indevidamente.

### RNF-07 — Clareza das mensagens de erro

**Descrição:** As mensagens de erro devem ser claras e orientar o usuário sobre como corrigir o problema ou qual ação realizar em seguida.

**Classificação:** Usabilidade.

**Justificativa:** Facilitar o uso do sistema por compradores, vendedores e administradores, reduzindo dúvidas durante as operações.

**Critérios de aceitação:**
- As mensagens devem explicar o problema em linguagem simples.
- Quando houver uma correção possível, a mensagem deve orientar o usuário.
- Erros de preenchimento devem identificar os campos que precisam ser corrigidos.
- As mensagens não devem expor senhas, dados pessoais ou detalhes técnicos sensíveis.
- As mensagens devem seguir um padrão consistente nas principais funcionalidades.

**Histórias relacionadas:** US01 — Pesquisar produtos agrícolas; US02 — Filtrar produtos; US03 — Favoritar produtos; US07 — Cadastrar produtos agrícolas; US08 — Cadastrar equipamentos agrícolas; US09 — Editar produtos; US10 — Alterar disponibilidade dos produtos; US11 — Entrar em contato com o produtor; US12 — Receber mensagens; US14 — Criar uma conta; US15 — Editar dados do perfil; US16 — Completar perfil de produtor; US18 — Aprovar ou reprovar anúncios; US19 — Denunciar anúncios inadequados; US20 — Remover anúncios inadequados.

**Decisão arquitetural — DA-07:** Padronizar o tratamento de erros e as mensagens exibidas na interface, mantendo detalhes técnicos em registros internos protegidos.

**Justificativa da decisão:** A padronização facilita a compreensão dos erros e a correção dos problemas, sem expor informações internas do sistema.

## 3. Resumo e classificação dos requisitos

| ID | Requisito | Classificação |
|---|---|---|
| RNF-01 | Desempenho nas buscas | Desempenho |
| RNF-02 | Otimização de imagens | Desempenho e eficiência |
| RNF-03 | Controle de acesso por perfil | Segurança |
| RNF-04 | Proteção de dados pessoais | Segurança e privacidade |
| RNF-05 | Funcionamento em conexões instáveis | Disponibilidade e tolerância a falhas |
| RNF-06 | Confiabilidade e integridade dos dados | Confiabilidade e integridade |
| RNF-07 | Clareza das mensagens de erro | Usabilidade |

## 4. Matriz de rastreabilidade entre RNFs e histórias de usuário

A matriz relaciona os requisitos não funcionais às histórias de usuário que podem ser afetadas por eles. As associações devem ser confirmadas com base nas descrições e nos critérios de aceitação do backlog.

| RNF | Histórias de usuário relacionadas |
|---|---|
| RNF-01 | US01, US02, US03, US04, US06 |
| RNF-02 | US07, US08, US09 |
| RNF-03 | US07, US08, US09, US10, US14, US15, US16, US17, US18, US19, US20 |
| RNF-04 | US11, US12, US13, US14, US15, US16 |
| RNF-05 | US01, US02, US04, US05, US07, US09, US10, US11, US12, US13, US15, US16 |
| RNF-06 | US03, US07, US08, US09, US10, US11, US12, US13, US14, US15, US16, US18, US19, US20 |
| RNF-07 | US01, US02, US03, US07, US08, US09, US10, US11, US12, US14, US15, US16, US18, US19, US20 |

### 4.1. Referência das histórias de usuário

| ID | História de usuário |
|---|---|
| US01 | Pesquisar produtos agrícolas |
| US02 | Filtrar produtos |
| US03 | Favoritar produtos |
| US04 | Visualizar informações do produto |
| US05 | Visualizar perfil do produtor |
| US06 | Comparar produtos |
| US07 | Cadastrar produtos agrícolas |
| US08 | Cadastrar equipamentos agrícolas |
| US09 | Editar produtos |
| US10 | Alterar disponibilidade dos produtos |
| US11 | Entrar em contato com o produtor |
| US12 | Receber mensagens |
| US13 | Visualizar conversas |
| US14 | Criar uma conta |
| US15 | Editar dados do perfil |
| US16 | Completar perfil de produtor |
| US17 | Visualizar anúncios |
| US18 | Aprovar ou reprovar anúncios |
| US19 | Denunciar anúncios inadequados |
| US20 | Remover anúncios inadequados |

### 4.2. Justificativa da rastreabilidade

- **RNF-01:** relaciona-se às funcionalidades de pesquisa, filtragem, visualização e comparação, nas quais o tempo de resposta afeta a experiência do consumidor.
- **RNF-02:** relaciona-se ao cadastro e à edição de produtos que podem envolver o envio de imagens.
- **RNF-03:** relaciona-se às ações que exigem permissões específicas de compradores, vendedores e administradores.
- **RNF-04:** relaciona-se ao cadastro e gerenciamento de contas, perfis e comunicações que envolvam dados pessoais.
- **RNF-05:** relaciona-se às consultas e operações que possam precisar de suporte a conexões instáveis. A disponibilidade offline deve ser definida para cada funcionalidade.
- **RNF-06:** relaciona-se às operações que precisam preservar a consistência dos dados e tratar falhas ou solicitações repetidas.
- **RNF-07:** relaciona-se às funcionalidades que podem apresentar erros de validação, conectividade, autorização ou processamento.

Uma história deve ser associada a um RNF quando existir uma relação verificável entre o requisito de qualidade e o comportamento esperado da funcionalidade.

## 5. Relação entre requisitos e decisões arquiteturais

As decisões propostas demonstram como as necessidades de qualidade influenciam a solução técnica do Greenmify.

|Decisão| RNF    | Solução técnica                                   | Benefício esperado                     |
|-------|--------|---------------------------------------------------|----------------------------------------|
| DA-01 | RNF-01 | Otimização de consultas, índices e paginação      | Redução do tempo de resposta           |
| DA-02 | RNF-02 | Validação e otimização automática de imagens      | Menor consumo de armazenamento e dados |
| DA-03 | RNF-03 | Autenticação e autorização no servidor            | Prevenção de acessos indevidos         |
| DA-04 | RNF-04 | Criptografia e gerenciamento seguro de chaves     | Maior proteção dos dados pessoais      |
| DA-05 | RNF-05 | Armazenamento local e sincronização               | Melhor suporte a conexões instáveis    |
| DA-06 | RNF-06 | Transações, validações e tratamento de repetições | Preservação da integridade dos dados   |
| DA-07 | RNF-07 | Tratamento padronizado de erros                   | Mensagens mais claras e consistentes   |


## 6. Critérios de validação

A equipe deve verificar os requisitos por meio de testes e revisões:

- **Desempenho:** medir o tempo de resposta das buscas em condições de teste documentadas.
- **Otimização de imagens:** verificar o processamento automático e a qualidade visual.
- **Segurança:** testar permissões por perfil e revisar a proteção dos dados pessoais.
- **Conectividade:** simular perda e restabelecimento da conexão e testar a sincronização.
- **Integridade:** testar falhas e solicitações repetidas em operações críticas.
- **Usabilidade:** revisar as mensagens de erro e verificar se orientam o usuário.
