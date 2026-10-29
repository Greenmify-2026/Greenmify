# Greenmify — Requisitos Não Funcionais

## Integrantes do grupo

- João Pedro Calaça Vasconcelos
- João Gabriel Gomes de Sousa
- Victor Araújo Pacheco de Miranda
- Heitor José Gondim Brito

## 1. Requisitos Não Funcionais

### RNF-01 — Desempenho nas buscas

As buscas de produtos devem retornar resultados em até 2 segundos, nas condições de teste definidas pela equipe.

**Justificativa:** Permitir que os consumidores encontrem produtos rapidamente, melhorando a experiência de navegação.

**Critérios de aceitação:**
- As buscas devem retornar resultados em até 2 segundos nas condições de teste acordadas.
- Os testes devem incluir pesquisas por nome e aplicação de filtros.
- O tempo de resposta deve ser medido por testes de desempenho.

### RNF-02 — Otimização de imagens

As imagens dos produtos devem ser compactadas e otimizadas automaticamente durante o envio, mantendo qualidade visual adequada.

**Justificativa:** Reduzir o consumo de armazenamento e de dados móveis, além de melhorar o carregamento das páginas.

**Critérios de aceitação:**
- As imagens devem ser otimizadas automaticamente durante o upload.
- A qualidade visual deve permitir identificar o produto.
- O sistema deve informar falhas no envio ou processamento.
- A imagem não deve ser apresentada como publicada antes da conclusão do processo.

### RNF-03 — Controle de acesso por perfil

O sistema deve restringir funcionalidades e dados conforme as permissões dos perfis de comprador, vendedor e administrador.

**Justificativa:** Impedir acessos indevidos e garantir que cada usuário execute apenas ações autorizadas.

**Critérios de aceitação:**
- Cada perfil deve acessar somente as funcionalidades autorizadas.
- Vendedores devem gerenciar apenas os próprios produtos.
- A aprovação e a remoção de anúncios devem ser restritas a usuários autorizados.
- Tentativas de acesso não autorizado devem ser bloqueadas no servidor.

### RNF-04 — Proteção de dados pessoais

Dados pessoais, como CPF e endereço, devem ser protegidos por criptografia e controles de acesso adequados.

**Justificativa:** Reduzir o risco de exposição indevida de informações e atender à legislação aplicável, incluindo a LGPD.

**Critérios de aceitação:**
- Dados sensíveis devem ser protegidos durante o armazenamento.
- A transmissão de dados pessoais deve utilizar comunicação protegida por TLS.
- O acesso deve ser limitado a usuários e operações autorizados.
- As chaves criptográficas devem ser gerenciadas separadamente dos dados protegidos.

### RNF-05 — Funcionamento em conexões instáveis

O sistema deve oferecer suporte a conexões instáveis, permitindo acesso offline parcial e retomada das operações compatíveis após o restabelecimento da conexão.

**Justificativa:** Facilitar o uso do Greenmify por produtores rurais em regiões com acesso limitado à internet.

**Critérios de aceitação:**
- O sistema deve informar quando a conexão estiver indisponível.
- Informações previamente armazenadas devem continuar acessíveis offline quando previsto.
- Operações que dependam do servidor devem indicar quando não puderem ser concluídas.
- As operações compatíveis devem ser sincronizadas após o restabelecimento da conexão.
- A sincronização deve tratar conflitos e evitar duplicações.

### RNF-06 — Confiabilidade e integridade dos dados

O sistema deve tratar falhas durante operações críticas, preservando a consistência dos dados e evitando perdas ou duplicações indevidas.

**Justificativa:** Proteger informações de produtos, disponibilidade, contas, mensagens e demais operações importantes para o marketplace.

**Critérios de aceitação:**
- Operações críticas devem preservar a consistência dos dados.
- Falhas não devem deixar operações parcialmente confirmadas sem tratamento.
- Solicitações repetidas devem ser tratadas para evitar duplicações quando aplicável.
- O sistema deve informar quando uma operação não puder ser concluída.
- Devem existir mecanismos de recuperação e registro de falhas.

### RNF-07 — Clareza das mensagens de erro

As mensagens de erro devem ser claras e orientar o usuário sobre como corrigir o problema ou qual ação realizar em seguida.

**Justificativa:** Facilitar o uso do sistema e reduzir dúvidas durante as operações.

**Critérios de aceitação:**
- As mensagens devem explicar o problema em linguagem simples.
- Quando houver uma correção possível, devem orientar o usuário.
- Erros de preenchimento devem identificar os campos que precisam ser corrigidos.
- As mensagens não devem expor dados pessoais ou detalhes técnicos sensíveis.
- As mensagens devem seguir um padrão consistente.

## 2. Classificação dos RNFs

| ID | Requisito | Classificação |
|---|---|---|
| RNF-01 | Desempenho nas buscas | Desempenho |
| RNF-02 | Otimização de imagens | Desempenho e eficiência |
| RNF-03 | Controle de acesso por perfil | Segurança |
| RNF-04 | Proteção de dados pessoais | Segurança e privacidade |
| RNF-05 | Funcionamento em conexões instáveis | Disponibilidade e tolerância a falhas |
| RNF-06 | Confiabilidade e integridade dos dados | Confiabilidade e integridade |
| RNF-07 | Clareza das mensagens de erro | Usabilidade |

## 3. Histórias de usuário relacionadas

| RNF | Histórias de usuário |
|---|---|
| RNF-01 | US01 — Pesquisar produtos agrícolas; US02 — Filtrar produtos; US03 — Favoritar produtos; US04 — Visualizar informações do produto; US06 — Comparar produtos. |
| RNF-02 | US07 — Cadastrar produtos agrícolas; US08 — Cadastrar equipamentos agrícolas; US09 — Editar produtos. |
| RNF-03 | US07 — Cadastrar produtos agrícolas; US08 — Cadastrar equipamentos agrícolas; US09 — Editar produtos; US10 — Alterar disponibilidade dos produtos; US14 — Criar uma conta; US15 — Editar dados do perfil; US16 — Completar perfil de produtor; US17 — Visualizar anúncios; US18 — Aprovar ou reprovar anúncios; US19 — Denunciar anúncios inadequados; US20 — Remover anúncios inadequados. |
| RNF-04 | US11 — Entrar em contato com o produtor; US12 — Receber mensagens; US13 — Visualizar conversas; US14 — Criar uma conta; US15 — Editar dados do perfil; US16 — Completar perfil de produtor. |
| RNF-05 | US01 — Pesquisar produtos agrícolas; US02 — Filtrar produtos; US04 — Visualizar informações do produto; US05 — Visualizar perfil do produtor; US07 — Cadastrar produtos agrícolas; US09 — Editar produtos; US10 — Alterar disponibilidade dos produtos; US11 — Entrar em contato com o produtor; US12 — Receber mensagens; US13 — Visualizar conversas; US15 — Editar dados do perfil; US16 — Completar perfil de produtor. |
| RNF-06 | US03 — Favoritar produtos; US07 — Cadastrar produtos agrícolas; US08 — Cadastrar equipamentos agrícolas; US09 — Editar produtos; US10 — Alterar disponibilidade dos produtos; US11 — Entrar em contato com o produtor; US12 — Receber mensagens; US13 — Visualizar conversas; US14 — Criar uma conta; US15 — Editar dados do perfil; US16 — Completar perfil de produtor; US18 — Aprovar ou reprovar anúncios; US19 — Denunciar anúncios inadequados; US20 — Remover anúncios inadequados. |
| RNF-07 | US01 — Pesquisar produtos agrícolas; US02 — Filtrar produtos; US03 — Favoritar produtos; US07 — Cadastrar produtos agrícolas; US08 — Cadastrar equipamentos agrícolas; US09 — Editar produtos; US10 — Alterar disponibilidade dos produtos; US11 — Entrar em contato com o produtor; US12 — Receber mensagens; US14 — Criar uma conta; US15 — Editar dados do perfil; US16 — Completar perfil de produtor; US18 — Aprovar ou reprovar anúncios; US19 — Denunciar anúncios inadequados; US20 — Remover anúncios inadequados. |

## 4. Decisões arquiteturais

| ID | Decisão arquitetural | RNF relacionado |
|---|---|---|
| DA-01 | Otimizar consultas ao banco de dados e avaliar o uso de índices e paginação. | RNF-01 |
| DA-02 | Implementar processamento de imagens no upload, com validação de formato e tamanho. | RNF-02 |
| DA-03 | Implementar autenticação e autorização por perfil no servidor. | RNF-03 |
| DA-04 | Adotar criptografia em repouso e em trânsito, com gerenciamento seguro de chaves. | RNF-04 |
| DA-05 | Definir armazenamento local, funcionalidades offline e sincronização com o servidor. | RNF-05 |
| DA-06 | Utilizar transações, validações de integridade e mecanismos para evitar duplicações em operações críticas. | RNF-06 |
| DA-07 | Padronizar o tratamento de erros e as mensagens exibidas na interface. | RNF-07 |

## 5. Justificativas das decisões

- **DA-01:** A otimização das consultas, os índices e a paginação podem reduzir o tempo de resposta das buscas.
- **DA-02:** O processamento automático de imagens reduz o consumo de armazenamento e de dados sem exigir ações adicionais do usuário.
- **DA-03:** A autorização no servidor impede que usuários contornem as restrições da interface para executar ações não permitidas.
- **DA-04:** A criptografia e o gerenciamento seguro de chaves reduzem o risco de exposição de dados pessoais durante o armazenamento e a transmissão.
- **DA-05:** O armazenamento local permite acessar informações disponíveis sem conexão, enquanto a sincronização recupera alterações pendentes e trata conflitos.
- **DA-06:** As transações e validações ajudam a preservar a consistência dos dados e a tratar falhas e solicitações repetidas.
- **DA-07:** A padronização das mensagens facilita a compreensão dos erros e orienta o usuário sem expor informações técnicas sensíveis.

## 6. Relações de rastreabilidade

A rastreabilidade demonstra como os requisitos não funcionais se relacionam às histórias de usuário e às decisões arquiteturais.

| RNF | Histórias relacionadas | Decisão arquitetural |
|---|---|---|
| RNF-01 | US01, US02, US03, US04, US06 | DA-01 |
| RNF-02 | US07, US08, US09 | DA-02 |
| RNF-03 | US07, US08, US09, US10, US14, US15, US16, US17, US18, US19, US20 | DA-03 |
| RNF-04 | US11, US12, US13, US14, US15, US16 | DA-04 |
| RNF-05 | US01, US02, US04, US05, US07, US09, US10, US11, US12, US13, US15, US16 | DA-05 |
| RNF-06 | US03, US07, US08, US09, US10, US11, US12, US13, US14, US15, US16, US18, US19, US20 | DA-06 |
| RNF-07 | US01, US02, US03, US07, US08, US09, US10, US11, US12, US14, US15, US16, US18, US19, US20 | DA-07 |
