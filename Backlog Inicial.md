# Universidade Católica de Pernambuco
## Graduação em Ciência da Computação

**Autores:**
- Heitor José Gondim Brito
- João Gabriel Gomes de Sousa
- João Pedro Calaça Vasconcelos
- Vitor Araújo Pacheco de Miranda

# Greenmify
## Backlog inicial do marketplace agrícola

**Recife — 2026**

---

## Apresentação do trabalho

**Greenmify: backlog inicial do marketplace agrícola**

Trabalho apresentado à disciplina de Processos e Requisitos de Software, do curso de Ciência da Computação da Universidade Católica de Pernambuco, como requisito para avaliação da disciplina.

**Professora:** Ivna Cristine Brasileiro Valença

**Recife — 2026**

---

## 1. Produto

O produto consiste em um marketplace digital voltado ao setor agrícola, com o objetivo de conectar produtores rurais e consumidores em uma plataforma para divulgação, pesquisa e comercialização de produtos e equipamentos agrícolas.

## 2. Problemas

- Dificuldade dos produtores em divulgar seus produtos.
- Dificuldade dos consumidores em encontrar produtos agrícolas.
- Informações espalhadas em diferentes canais.
- Dificuldade de conhecer o produtor e seus produtos.
- Falta de uma plataforma centralizada para essa interação.

## 3. Personas

### 3.1 Consumidor

É o usuário que acessa o marketplace em busca de produtos e equipamentos agrícolas para atender às suas necessidades. Seu objetivo é encontrar produtos de forma rápida, comparar opções e obter informações antes de realizar uma compra. Suas principais necessidades são uma busca eficiente, informações claras sobre os produtos e facilidade para entrar em contato com os produtores. Suas principais dificuldades são encontrar produtos específicos, comparar diferentes opções e obter informações confiáveis sobre os anúncios.

### 3.2 Produtor Rural

É o usuário que utiliza o marketplace para divulgar e comercializar seus produtos e equipamentos agrícolas. Seu objetivo é alcançar potenciais consumidores e manter seus anúncios atualizados. Suas principais necessidades são facilidade para cadastrar produtos, gerenciar informações e disponibilidade dos anúncios e se comunicar com os interessados. Suas principais dificuldades são divulgar seus produtos para um público maior, manter os anúncios atualizados e acompanhar as dúvidas e contatos dos consumidores.

### 3.3 Administrador

É o responsável por gerenciar e manter o funcionamento adequado do marketplace. Seu objetivo é garantir que os anúncios e usuários estejam de acordo com as regras da plataforma. Suas principais necessidades são visualizar, analisar, aprovar, reprovar e remover anúncios inadequados, além de acompanhar denúncias. Sua principal dificuldade é manter a plataforma organizada e segura, identificando e tratando conteúdos que possam prejudicar a experiência dos usuários.

## 4. Stakeholders

1. **Consumidores:** possuem interesse no marketplace por utilizarem a plataforma para pesquisar produtos e equipamentos agrícolas, comparar opções e entrar em contato com produtores.
2. **Produtores rurais:** possuem interesse direto no sistema, pois utilizam a plataforma para divulgar seus produtos e equipamentos e alcançar potenciais consumidores.
3. **Administradores da plataforma:** são responsáveis pela gestão e moderação do marketplace, garantindo que os anúncios e usuários estejam de acordo com as regras estabelecidas.
4. **Equipe de desenvolvimento:** responsável por projetar, desenvolver, testar e manter o sistema, garantindo que as funcionalidades atendam às necessidades dos usuários.
5. **Proprietários ou responsáveis pelo marketplace:** possuem interesse no funcionamento e nos resultados da plataforma, buscando oferecer um serviço funcional, seguro e que atenda aos objetivos do negócio.

## 5. Product Backlog

Reúne as principais funcionalidades do marketplace, organizadas em seis épicos. As histórias foram priorizadas utilizando a técnica MoSCoW, considerando a importância de cada funcionalidade para o funcionamento do aplicativo.

| ID | Épico | História | Prioridade |
|---|---|---|---|
| US01 | Busca e descoberta de produtos | Pesquisar produtos agrícolas | Must |
| US02 | Busca e descoberta de produtos | Filtrar produtos | Must |
| US03 | Busca e descoberta de produtos | Favoritar produtos | Could |
| US04 | Visualização e informações dos produtos | Visualizar informações do produto | Must |
| US05 | Visualização e informações dos produtos | Visualizar perfil do produtor | Should |
| US06 | Visualização e informações dos produtos | Comparar produtos | Should |
| US07 | Cadastro e gerenciamento de produtos | Cadastrar produtos agrícolas | Must |
| US08 | Cadastro e gerenciamento de produtos | Cadastrar equipamentos agrícolas | Must |
| US09 | Cadastro e gerenciamento de produtos | Editar produtos | Should |
| US10 | Cadastro e gerenciamento de produtos | Alterar disponibilidade dos produtos | Must |
| US11 | Comunicação entre consumidor e vendedor | Entrar em contato com o produtor | Must |
| US12 | Comunicação entre consumidor e vendedor | Receber mensagens | Must |
| US13 | Comunicação entre consumidor e vendedor | Visualizar conversas | Should |
| US14 | Gerenciamento de usuários e perfis | Criar uma conta | Must |
| US15 | Gerenciamento de usuários e perfis | Editar dados do perfil | Should |
| US16 | Gerenciamento de usuários e perfis | Completar perfil de produtor | Should |
| US17 | Moderação e segurança | Visualizar anúncios | Must |
| US18 | Moderação e segurança | Aprovar ou reprovar anúncios | Must |
| US19 | Moderação e segurança | Denunciar anúncios inadequados | Should |
| US20 | Moderação e segurança | Remover anúncios inadequados | Must |

### 5.1 Legenda da priorização MoSCoW

- **Must — Deve ter/Essencial:** funcionalidades necessárias para o funcionamento básico do aplicativo.
- **Should — Deveria ter/Importante:** funcionalidades importantes, mas que não impedem o funcionamento inicial do sistema.
- **Could — Poderia ter/Desejável:** funcionalidades que agregam valor, mas não são essenciais.
- **Won't — Não terá nesta versão:** funcionalidades que ficam fora do escopo da versão atual.

## 6. Critérios de Aceitação

### US01
O sistema deve permitir pesquisar produtos por nome ou palavra-chave e apresentar resultados relacionados.

### US02
O sistema deve permitir filtrar produtos por categoria e faixa de preço.

### US03
O sistema deve permitir adicionar produtos aos favoritos e acessá-los posteriormente.

### US04
O sistema deve apresentar informações como nome, descrição, preço e disponibilidade do produto.

### US05
O sistema deve permitir visualizar as informações e os produtos cadastrados pelo produtor.

### US06
O sistema deve permitir selecionar produtos e visualizar suas informações para comparação.

### US07
O produtor deve conseguir cadastrar um produto informando seus dados principais.

### US08
O produtor deve conseguir cadastrar equipamentos agrícolas com suas respectivas informações.

### US09
O produtor deve conseguir alterar as informações de seus produtos cadastrados.

### US10
O produtor deve conseguir alterar a disponibilidade de um produto, indicando se está disponível ou esgotado.

### US11
O consumidor deve conseguir iniciar uma conversa com o produtor a partir de um produto.

### US12
O produtor deve receber as mensagens enviadas pelos consumidores.

### US13
O produtor deve conseguir visualizar suas conversas e as mensagens recebidas.

### US14
O visitante deve conseguir criar uma conta preenchendo os dados obrigatórios.

### US15
O usuário deve conseguir visualizar e editar seus dados pessoais e informações do perfil.

### US16
O produtor deve conseguir adicionar informações sobre sua atividade e seu negócio ao perfil.

### US17
O administrador deve conseguir visualizar os anúncios cadastrados na plataforma.

### US18
O administrador deve conseguir aprovar ou reprovar anúncios antes de sua publicação.

### US19
O consumidor deve conseguir denunciar um anúncio e informar o motivo da denúncia.

### US20
O administrador deve conseguir remover anúncios considerados inadequados.

## 7. Justificativa Técnica

O desenvolvimento do marketplace foi planejado com o objetivo de criar uma solução que facilite a relação entre consumidores e produtores rurais. A proposta é reunir em uma única plataforma funcionalidades que permitam aos consumidores encontrar produtos e equipamentos agrícolas, consultar informações, conhecer os produtores e entrar em contato com eles. Para os produtores, o sistema oferece recursos para cadastrar e gerenciar seus produtos e divulgar seus negócios.

A organização do sistema em épicos e histórias de usuário foi escolhida para facilitar o planejamento e o desenvolvimento do projeto. Os épicos agrupam funcionalidades que possuem objetivos semelhantes, enquanto as histórias de usuário descrevem cada funcionalidade a partir da perspectiva de quem irá utilizá-la. Essa divisão torna os requisitos mais claros e facilita a distribuição das tarefas entre os integrantes da equipe.

O Product Backlog foi utilizado para reunir e organizar as funcionalidades inicialmente definidas para o produto. A partir dele, a equipe consegue visualizar o que precisa ser desenvolvido e acompanhar a evolução do projeto. As histórias também podem ser movimentadas e organizadas no GitHub Projects, permitindo acompanhar quais atividades ainda estão no backlog, quais estão em desenvolvimento e quais já foram concluídas.

Para definir a importância de cada funcionalidade, foi utilizada a técnica de priorização MoSCoW. As funcionalidades classificadas como Must são consideradas essenciais para o funcionamento inicial do marketplace, como criar uma conta, pesquisar produtos, visualizar informações, cadastrar produtos e permitir a comunicação entre consumidores e produtores. As funcionalidades Should possuem importância para melhorar a experiência dos usuários, mas não impedem o funcionamento básico do sistema. Já as funcionalidades Could são recursos adicionais que podem ser desenvolvidos posteriormente.

A definição das funcionalidades também levou em consideração as diferentes necessidades dos usuários identificados. O consumidor precisa encontrar produtos de maneira simples e ter informações suficientes para tomar suas decisões. O produtor precisa de uma forma prática de divulgar seus produtos, atualizar seus anúncios e responder aos interessados. O administrador, por sua vez, precisa de ferramentas para acompanhar e moderar os anúncios da plataforma.

Os critérios de aceitação foram definidos para cada história de usuário com o objetivo de tornar possível verificar se a funcionalidade foi desenvolvida corretamente. Eles ajudam a equipe a entender o que deve acontecer no sistema e servem como uma referência durante os testes. Dessa forma, o desenvolvimento não fica baseado apenas na descrição da história, mas também em condições que podem ser verificadas na prática.

A utilização dessas técnicas contribui para um desenvolvimento mais organizado e reduz a possibilidade de funcionalidades importantes serem esquecidas. Além disso, a priorização permite que a equipe concentre seus esforços inicialmente nos recursos que possuem maior impacto no funcionamento do produto, deixando funcionalidades complementares para etapas posteriores.

Por fim, a estrutura adotada permite que o projeto seja desenvolvido de forma incremental. Conforme novas necessidades forem identificadas durante o desenvolvimento, o Product Backlog poderá ser atualizado, permitindo adicionar, alterar ou reorganizar histórias de usuário. Assim, o planejamento não fica limitado às funcionalidades definidas inicialmente e pode acompanhar a evolução do marketplace.

## 8. Conclusão

A elaboração do Product Backlog permitiu organizar as principais funcionalidades do marketplace de forma clara e estruturada. A definição das personas, stakeholders, histórias de usuário, prioridades e critérios de aceitação fornece uma base para o desenvolvimento do sistema e facilita o acompanhamento das próximas etapas do projeto.
