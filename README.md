# das-1-2025-2-a

## Aula 04/08

### Princípios de Projeto de Software - Capítulo 5

- **Abstração:** Representar algo do mundo real para resolver um problema.

- **Componentes do Sistema:**
  - **Controller:** API
  - **Entity:** Dados
  - **Repository:** Banco de Dados
  - **Service:** Lógica de negócios

- **Coesão no Código:**  
  Um código coeso é aquele que é fácil de entender e manter, pois executa uma única tarefa.

- **Inversão de Dependência:**  
  Quando uma classe controladora utiliza uma interface em vez de uma implementação concreta.

- **Herança:**  
  Exemplo: **Cachorro** e **Gato** herdam a classe **Animal**, mas possuem comportamentos diferentes.

- **Composição vs. Herança:**  
  Quando existem duas soluções, uma utilizando herança e outra composição, normalmente a composição é preferível.

- **Princípio Aberto/Fechado:**  
  Uma classe deve estar **aberta para extensões** (novas funcionalidades) e **fechada para modificações** (alterações no código existente).

- **Princípio da Inversão de Dependências:**  
  Uma classe deve depender de abstrações (interfaces), e não de implementações concretas.

- **Princípio de Demeter (Princípio do Menor Conhecimento):**  
  A classe deve interagir apenas com seu próprio código ou com objetos passados como parâmetro, evitando variáveis globais frágeis.

- **Liskov Substitution Principle (LSP):**  
  O código das classes filhas deve ser compatível com o das classes pais, permitindo que sejam substituídas sem afetar o comportamento do sistema.

- **Static Instance:**  
  Similar a uma variável global, usada para manter o estado de um objeto.

---

## Aula 01/09

### Expectativas do Arquiteto:

- **Tomar Decisões Desafiadoras em Arquitetura:**  
  O arquiteto é responsável por tomar decisões complexas sobre a arquitetura do sistema.

- **Orientar a Equipe nas Escolhas Tecnológicas:**  
  O arquiteto deve guiar a equipe nas decisões sobre tecnologias, justificando as escolhas com base na experiência.

- **Analisar Continuamente a Arquitetura:**  
  Revisar o código e identificar áreas que necessitam de refatoração, além de determinar o melhor momento para fazê-la.

- **Manter-se Atualizado sobre Tendências Tecnológicas:**  
  O arquiteto deve estar ciente das novas tecnologias e como elas podem ser aplicadas ao sistema.

- **Garantir Conformidade com as Decisões:**  
  Garantir que os desenvolvedores sigam os padrões definidos, usando testes de código para garantir a qualidade.

- **Exposição e Experiência Diversificada:**  
  A experiência acumulada é essencial para tomar decisões arquiteturais bem informadas.

- **Conhecimento sobre o Domínio de Negócio:**  
  Ter uma compreensão sólida do contexto de negócios é fundamental para projetar soluções eficazes.

- **Habilidades Interpessoais:**  
  O arquiteto deve saber trabalhar bem com outras pessoas, assumindo o papel de líder para inspirar e motivar a equipe.

- **Entender e Lidar com Questões Políticas:**  
  O arquiteto deve ser capaz de influenciar decisões e gerenciar as questões políticas envolvidas no processo de arquitetura.

---

### Operações/DevOps:

- **DevOps:**  
  Integra as equipes de desenvolvimento e operações para entregar valor ao cliente de forma mais rápida e eficiente.

- **Cultura e Colaboração:**  
  O DevOps é visto como uma cultura em que todos participam de cada fase do processo, e, se o sistema falhar, todos trabalham juntos para resolver o problema.

- **Planejamento:**  
  Desenvolver planos detalhados com tarefas divididas em ciclos curtos de trabalho (como no Scrum).

- **Integração Contínua:**  
  Manter um repositório centralizado e confiável de código.

- **Feedback:**  
  O ciclo de desenvolvimento é contínuo, com cada iteração trazendo aprendizados para aprimorar o processo.

---

## Aula 02/09

### Diferença entre Arquitetos e Desenvolvedores:

- **Desenvolvedor:** Foca na **profundidade**, especializando-se em partes específicas da tecnologia.
- **Arquiteto:** Foca na **amplitude**, entendendo uma variedade maior de soluções e contextos para resolver problemas de forma eficaz.

Ao transitar de desenvolvedor para arquiteto, é importante mudar a forma de adquirir conhecimento, equilibrando profundidade e amplitude.

---

## Aula 08/09

### Compensações (Trade-offs):

Ao definir uma arquitetura, é impossível atender a todos os requisitos simultaneamente. Como afirma o princípio:  
*"Não existem respostas certas ou erradas, apenas compensações."*

---

### Arquitetura Baseada em Tópicos:

- **Tópico:**  
  Um tópico é como um grupo de família no WhatsApp, organizado para facilitar a comunicação.

- **Padrão Observer:**  
  Funciona com 1 Publisher (emissor) e múltiplos Subscribers (assinantes).

- **Funcionamento:**  
  Os assinantes se inscrevem no broker (tópico), que envia mensagens aos inscritos. Se o tópico ficar fora do ar, as mensagens podem ser perdidas.

- **Vantagens:**
  - Menor acoplamento entre os componentes.
  - Rastreabilidade de problemas reduzida.

---

### Arquitetura Baseada em Listas:

- **Fluxo de Comunicação:**  
  **Sender <-> Fila <-> Receiver**. As mensagens são enfileiradas para entrega.

- **Operações:**  
  - **Enqueue:** Coloca a mensagem na fila.
  - **Dequeue:** Retira a mensagem da fila.

- **Ponto a Ponto:**  
  Cada receiver tem uma fila própria, isolando a comunicação entre os receivers.

- **Vantagens:**
  - Garantia de entrega na ordem correta.
  - Fila como buffer, armazenando mensagens até que sejam processadas.

- **Desvantagens:**  
  - Adicionar um novo receiver exige a criação de uma fila exclusiva, o que pode impactar o sender e aumentar o acoplamento.
  - Rastreabilidade de problemas mais complexa.

---
