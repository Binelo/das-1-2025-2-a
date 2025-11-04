# das-1-2025-2-a

## Aula 04/08

### Princípios de Projeto de Software - Capítulo 5

- **Abstração:** Representa elementos do mundo real para resolver um problema de forma mais simples e organizada.

- **Componentes do Sistema:**
  - **Controller:** Interface da API.
  - **Entity:** Estrutura dos dados.
  - **Repository:** Comunicação com o banco de dados.
  - **Service:** Implementa a lógica de negócios.

- **Coesão no Código:**  
  Um código coeso realiza uma única tarefa, o que o torna mais fácil de entender, testar e manter.

- **Inversão de Dependência:**  
  Uma classe deve depender de **interfaces** (abstrações), e não de implementações concretas.

- **Herança:**  
  Exemplo: **Cachorro** e **Gato** herdam a classe **Animal**, mas cada um implementa comportamentos distintos.

- **Composição vs. Herança:**  
  Quando possível, prefira **composição**, pois ela oferece mais flexibilidade e reduz o acoplamento entre classes.

- **Princípio Aberto/Fechado:**  
  Uma classe deve estar **aberta para extensão** (novas funcionalidades) e **fechada para modificação** (evitar alterar código existente).

- **Princípio de Demeter (Menor Conhecimento):**  
  Uma classe deve interagir apenas com seus próprios dados e objetos recebidos como parâmetros, evitando dependências externas desnecessárias.

- **Liskov Substitution Principle (LSP):**  
  Classes derivadas devem poder substituir as classes base sem quebrar o comportamento do sistema.

- **Static Instance:**  
  Similar a uma variável global, usada para manter o estado de um objeto durante a execução.

---

## Aula 01/09

### Expectativas do Arquiteto

- **Tomar Decisões Arquiteturais Complexas:**  
  Cabe ao arquiteto definir soluções técnicas e estruturais do sistema.

- **Orientar a Equipe:**  
  O arquiteto deve guiar as decisões tecnológicas, explicando suas escolhas com base em experiência e contexto.

- **Analisar e Melhorar a Arquitetura:**  
  É essencial revisar constantemente o código e identificar oportunidades de refatoração.

- **Atualização Contínua:**  
  Estar atento às novas tecnologias e tendências é parte fundamental da função.

- **Garantir Padrões e Qualidade:**  
  Verificar se o código segue os padrões definidos, utilizando práticas como revisões e testes automatizados.

- **Experiência e Versatilidade:**  
  A bagagem técnica e prática é o que sustenta boas decisões arquiteturais.

- **Conhecimento de Negócio:**  
  Entender o domínio do sistema é fundamental para propor soluções eficazes.

- **Habilidades Interpessoais:**  
  O arquiteto deve inspirar, orientar e colaborar com a equipe.

- **Gestão Política:**  
  Saber lidar com interesses e influenciar decisões faz parte da atuação profissional.

---

### Operações / DevOps

- **DevOps:**  
  Integra equipes de desenvolvimento e operação para entregar valor ao cliente com agilidade e qualidade.

- **Cultura e Colaboração:**  
  Todos são responsáveis pelo sucesso e falhas do sistema, é uma cultura de cooperação.

- **Planejamento Ágil:**  
  Tarefas são organizadas em ciclos curtos (como no Scrum), facilitando a adaptação.

- **Integração Contínua:**  
  Manter um repositório centralizado e estável para integração de código frequente.

- **Feedback Contínuo:**  
  O processo é iterativo, cada ciclo traz aprendizados e melhorias.

---

## Aula 02/09

### Diferença entre Arquitetos e Desenvolvedores

- **Desenvolvedor:** Aprofunda-se em tecnologias específicas, dominando detalhes técnicos.  
- **Arquiteto:** Possui visão ampla, compreendendo várias tecnologias e suas interações.

A transição de desenvolvedor para arquiteto exige equilíbrio entre profundidade e amplitude de conhecimento.

---

## Aula 08/09

### Compensações (Trade-offs)

Toda arquitetura exige **escolhas**, é impossível atender a todos os requisitos ao mesmo tempo.  
Como se diz:  
> “Não existem respostas certas ou erradas, apenas compensações.”

---

### Arquitetura Baseada em Tópicos

- **Tópico:**  
  Funciona como um grupo de mensagens (ex: grupo do WhatsApp) para comunicação entre sistemas.

- **Padrão Observer:**  
  Um **Publisher** envia mensagens que são recebidas por múltiplos **Subscribers**.

- **Funcionamento:**  
  Os assinantes se registram em um **broker**, que envia as mensagens. Caso o broker falhe, mensagens podem ser perdidas.

- **Vantagens:**
  - Reduz o acoplamento entre sistemas.
  - Facilita a comunicação assíncrona.

---

### Arquitetura Baseada em Filas (Queue-Based)

- **Fluxo:**  
  **Sender → Fila → Receiver**. As mensagens são enfileiradas para processamento posterior.

- **Operações:**
  - **Enqueue:** adiciona mensagem.
  - **Dequeue:** remove mensagem.

- **Ponto a Ponto:**  
  Cada receptor possui sua própria fila, isolando comunicações.

- **Vantagens:**
  - Garante ordem de entrega.
  - Fila atua como buffer de mensagens.

- **Desvantagens:**
  - Necessidade de múltiplas filas pode aumentar o acoplamento.
  - Rastreamento de falhas mais complexo.

---

# Segundo Bimestre

## Aula 29/09

### Padrão Circuit Breaker

- Utilizado em **sistemas distribuídos**, onde múltiplos serviços se comunicam via rede.
- Evita que chamadas fiquem presas indefinidamente em caso de falhas.
- Atua como um **disjuntor elétrico**, abrindo o circuito quando há falha.
- **Estados do Circuit Breaker:**
  - **Fechado:** Tudo funcionando normalmente.  
  - **Aberto:** Uma falha ocorreu, e novas tentativas são bloqueadas temporariamente.  
  - **Meio-aberto:** Testa periodicamente se o serviço voltou ao normal, se sim, retorna ao estado fechado.

Esse padrão ajuda a manter a **resiliência** do sistema e evita sobrecargas em serviços indisponíveis.

---

## Aula 06/10

### Características Arquiteturais

Uma **característica arquitetural** é um requisito não funcional que:

1. Representa uma preocupação fora do domínio do negócio.  
2. Impacta o design estrutural do sistema.  
3. É essencial para o sucesso da aplicação.

Essas características podem ser vistas como um triângulo de sustentação, cada uma apoia as demais.

- **Características Operacionais:** Desempenho, escalabilidade, elasticidade.  
- **Características Estruturais:** Configuração, extensibilidade, estabilidade, localização.  
- **Características Transversais:** Acessibilidade, armazenamento, autenticação, autorização.

Os termos nem sempre são precisos — alguns se sobrepõem, como **disponibilidade** e **confiabilidade**.  
A norma **ISO** fornece uma lista parcial dessas capacidades.

---

### Trade-offs e Arquitetura “Menos Pior”

Um software consegue suportar apenas algumas características ao mesmo tempo.  
Adicionar muitas pode gerar conflitos e soluções genéricas ineficientes.  
Por isso, arquiteturas devem ser **iterativas**, permitindo **mudanças graduais e controladas**.

---

## Aula 06/10

### CQRS – Command Query Responsibility Segregation

Separa as operações de **leitura** e **escrita** do banco de dados para melhorar desempenho.

- **Quando usar:**
  - Problemas de performance (limites de hardware atingidos).
  - Problemas de bloqueio (locks) em operações concorrentes.

**Funcionamento:**
- Há uma instância principal do banco para **escritas**.  
- Réplicas são criadas apenas para **leituras**.  
- As atualizações são **replicadas de forma assíncrona**, o que pode causar pequenos atrasos.

Esse padrão ajuda a escalar sistemas com alto volume de consultas.

---

## Aula 13/10

### Padrão Retry

Define uma estratégia para **tentar novamente** operações que falham.

- **Retry imediato:** tenta logo após a falha.  
- **Retry com atraso:** aguarda um intervalo antes de tentar novamente — o tempo pode aumentar exponencialmente a cada falha.  
- É importante definir **limites** para evitar tentativas infinitas.

---

### Estilos e Padrões Arquiteturais

Um sistema pode adotar mais de um padrão ao mesmo tempo.

- **Grande Bola de Lama:** Código desorganizado, sem planejamento, difícil de manter e evoluir.  
- **Arquitetura Monolítica:** Todo o sistema em uma única base de código.  
- **Arquitetura Unificada (Embedded):** Usada em dispositivos como geladeiras ou micro-ondas.  
- **Cliente/Servidor:** Funções divididas entre cliente e servidor.  
- **Desktop + Servidor de Banco:** Aplicações locais que acessam um banco central.  
- **Navegador + Servidor Web:** Clientes acessam via navegador, e o servidor processa as requisições e retorna páginas HTML.

---

## Aula 14/10

### Arquiteturas em Três Camadas

- **Monólito:** todas as funções dentro de um único sistema.  
- **Distribuído:** dividido em **microsserviços**.

Migrar de monólito para distribuído é recomendado quando há dificuldade de escalar ou implementar novas funções, mas nem sempre é a melhor opção.

#### Falácias de Sistemas Distribuídos

1. A rede é confiável  
2. A latência é zero  
3. A largura de banda é infinita  
4. A rede é segura  
5. A topologia nunca muda

#### Padrões em Sistemas Distribuídos

- **Log Distribuído:** Centraliza registros de logs.  
- **Transações Distribuídas:** Executam operações que envolvem múltiplos serviços.

---

## Aula 20/10

### Estilo de Arquitetura em Camadas (Capítulo 10)

A arquitetura em camadas é amplamente usada por ser simples, de baixo custo e fácil manutenção.

#### Topologia

Os componentes são organizados horizontalmente em camadas, cada uma com uma função específica:
1. **Apresentação**
2. **Negócios**
3. **Persistência**
4. **Banco de Dados**

Cada camada tem responsabilidades isoladas, facilitando o desenvolvimento paralelo e a manutenção.

#### Isolamento de Camadas

- **Camada Fechada:** só se comunica com a imediatamente inferior.  
- **Camada Aberta:** pode pular uma camada intermediária se necessário.  
Esse isolamento permite trocar uma camada sem impactar as demais.

#### Adição de Camadas

Adicionar novas camadas pode ajudar na integração ou especialização de funções.

#### Considerações Finais

- Boa escolha para sistemas simples ou com orçamento limitado.  
- Útil quando ainda se está definindo requisitos e domínios.  
- O **antipadrão Sinkhole** ocorre quando requisições passam por várias camadas sem processamento real.  
  - É aceitável em até **20%** dos casos.  
  - Se chegar a **80%**, é sinal de problemas arquiteturais.

---

## Aula 27/10

### Arquitetura Pipeline

Nesse modelo, o processamento ocorre **em sequência**, passando por etapas chamadas **filtros**.

Os principais tipos de filtros são:
- **Produtor:** gera os dados de entrada.  
- **Transformador:** modifica ou processa os dados.  
- **Verificador:** valida os resultados intermediários.  
- **Consumidor:** recebe e utiliza a saída final.

Essa arquitetura é útil quando o fluxo de dados pode ser dividido em etapas bem definidas e independentes.
