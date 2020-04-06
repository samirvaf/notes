# CTFL Notes

## Capítulo 1 - Fundamentos de teste

### 1.1 O que é teste?

- O teste de software é uma maneira de avaliar a qualidade do software e reduzir o risco de falha do software em operação.
- O processo de software não se resume em apenas executar e observar os resultados, ele envolve também diversas outras atividades como: planejamento de teste, análise, modelagem e implementação dos testes, relatórios de progresso e resultados dos testes e avaliação da qualidade de um objeto de teste.
- Testes que envolvem a execução do sistema ou componente a ser testado são chamados de testes dinâmicos, quando não envolvem a execução do software são chamados testes estáticos.
- Além de verificar se o sistema atende aos requisitos especificados, o processo de testes também contempla a validação que consiste em verificar se o sistema atenderá as necessidades do usuário e stakeholders em seu ambiente operacional.

### 1.1.2 Teste e depuração de código

- Teste e depuração de código são coisas diferentes. A execução de testes pode mostrar falhas causadas por defeitos no software. Depuração é a atividade de desenvolvimento que analisa, localiza e corrige esses defeitos.

### 1.2 Por que o teste é necessário?

- Contribuir para a qualidade de componentes/sistemas. Atender requisitos contratuais ou legais e aos padrões específicos do setor.

### 1.2.1 Contribuições do teste para o sucesso

- O uso de técnicas de testes pode reduzir de forma significativa a entrega de software com defeitos. Exemplos incluem: Ter testadores nas revisões de requisitos ou no refinamento das estórias de usuários, ter testadores trabalhando em conjunto com os projetistas do sistema para aumentar o entendimento de cada parte sobre o projeto e como testá-lo, testadores trabalhando em colaboração com os desenvolvedores afim de aumentar o entendimento de cada parte sobre o código e como testá-lo, ter testadores para verificar e validar o software antes de liberar para poder detectar falhas e suportar o processo de remoção de defeitos através da depuração de código.

### 1.2.3 Erros, defeitos e falhas

- Erro é o que uma pessoa comete (engano) que pode levar à introdução de um defeito (bug) no código de um software ou em algum outro produto de trabalho relacionado.
- A execução de um código defeituoso pode causar uma falha, mas não necessariamente em todas as circunstâncias. Exemplo, um conjunto específico de entradas ou pré-condições muito específicas.
- Além das falhas causadas por defeitos no código, falhas também podem ser causadas por condições ambientais. Exemplo, radiação, campos eletromagnéticos.

### 1.2.4 Defeitos, causas-raiz e efeitos

- As causas-raiz dos defeitos são as primeiras ações ou condições que contribuíram para a criação dos defeitos.
- Defeitos podem ser analisados para identificar suas causas-raiz, de modo a reduzir a ocorrência de defeitos similares no futuro.

### 1.3 Os sete princípios de testes

- O teste mostra a presença de defeitos, não sua ausência.
- Testes exaustivos são impossíveis.
- O teste inicial economiza tempo e dinheiro.
- Defeitos se agrupam
- Paradoxo do pesticida (Se os mesmos testes forem repetidos várias vezes, esses testes não encontraram novos defeitos).
- O teste depende do contexto.
- Ausência de erros é uma ilusão.

### 1.4 Processos de teste

- Não existe um processo universal de teste de software, mas há conjuntos comuns de atividades de teste sem as quais os testes terão menor probabilidade de atingir seus objetivos estabelecidos. Esses conjuntos de atividades de teste são um processo de teste.

### 1.4.1 Processo de teste no contexto

- Alguns fatores contextuais que influenciam o processo de teste de uma organização são por exemplo:

1. Modelo do ciclo de vida de desenvolvimento de software e metologias de projeto utilizados.
2. Níveis de teste e tipos de teste considerados.
3. Riscos de produto e projeto.
4. Domínio do negócio.
5. Algumas restrições operacionais como orçamentos e recursos, escalas de tempo, complexidade, requisitos contratuais e regulamentares.
6. Políticas e práticas organizacionais.
7. Normas internas e externas necessárias.

### 1.4.2 Atividades e tarefas de teste

- Planejamento do teste.
- Monitoramento e controle do teste.
- Análise do teste.
- Modelagem do teste.
- Implementação do teste.
- Execução do teste.
- Conclusão do teste.

### 1.4.3 Produtos de trabalho do teste

- Cada uma das atividades e tarefas de teste produz um produto de trabalho do teste. Estes podem variar de diversas formas, apesar do resultado final de um produto de teste representar o objetivo daquela etapa.

### 1.5 A Psicologia do teste

- Viés de confirmação impede que desenvolvedores enxerguem erros no próprio trabalho.
- É importante manter bons relacionamentos.
- Normalmente o tester é o portador das más notícias.
- Concentar em críticas contrutivas, se ater ao aspecto técnico dos erros, não relacionar à pessoa que o introduziu.
- Lembrar sempre do objetivo comum de sistemas de melhor qualidade.
- Enfatizar os benefícios do teste.
- Confirmar se a comunicação foi estabelecida, se você foi entendido e se entendeu o outro.

## Capítulo 2 - Teste durante o ciclo de desenvolvimento de software

### 2.1 Modelos de ciclo de vida de desenvolvimento de software
