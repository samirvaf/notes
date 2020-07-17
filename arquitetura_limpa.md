# Arquitetura Limpa


## Capítulo 1 - O que são design e arquitetura?

- Os dois termos são utilizados, normalmente design se refere a detalhes de baixo nível enquanto a arquitetura se preocupa com a descrição alto nível porém não existe diferença entre eles, são parte do mesmo todo e não existe uma linha que os separa claramente.
- O objetivo da arquitetura de software é minimizar os recursos humanos necessários para construir e manter um determinado sistema.
- A única maneira de seguir rápido é seguir bem, manter sempre a autoconfiança sob controle, não cair em ciladas do tipo: "depois posso voltar e arrumar esse código, nesse momento o mais importante é liberar o release logo".
- Desenvolvedores podem achar que a resposta para resolver problemas de um sistema que declinou a produtividade de toda uma equipe a zero é reescrever todo o sistema, na realidade o que é preciso é uma mudança na mentalidade, ou o novo sistema está fadado ao mesmo destino.

## Capítulo 2 - Um conto de dois valores

- Nesse capítulo o autor faz uma análise sobre a importância da arquitetura levantando em conta dois valores importantes, funcionalidade e capacidade de mudança.
- Infelizmente a maior parte dos desenvolvedores prioriza a funcionalidade ao invés de uma boa arquitetura, um argumento simples que demostra como essa atitude está incorreta é: se você me der um programa que não funciona mas que seja fácil de ser modificado eu posso fazê-lo funcionar e mantê-lo funcionando por muito tempo, em contrapartida se você me der um programa que funciona porém que seja difícil de ser modificado, o programa não funcionará assim que os requisitos mudarem.
- Colocar a arquitetura em segundo plano parte do princípio que a funcionalidade é urgente, gerentes de negócio querem o software funcionando o quanto antes, porém a **importância** está acima da **urgência** (matriz de Eisenhower), e cabe a equipe de desenvolvimento lutar para garantir que a arquitetura seja entendida como prioridade considerando o longo prazo, vida útil do software.
- Se a arquitetura vier por último, então o sistema ficará cada vez mais caro para se desenvolver e, por fim, a mudança será praticamente impossível para parte ou para todo o sistema. 