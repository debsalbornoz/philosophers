# Philosophers

 <h1>Sobre</h1>

O projeto **Philosophers** da 42 é uma experiência prática que explora a concorrência e a sincronização na programação, fundamentando-se no célebre problema do "Jantar dos Filósofos" proposto por Edsger Dijkstra em 1965. Neste projeto, a vida de filósofos que se sentam à mesa para jantar é modelada, onde cada filósofo alterna entre os estados de pensar, comer e dormir. Para realizar suas refeições, os filósofos utilizam garfos, que são recursos compartilhados e limitados. O desafio central é garantir que todos os filósofos possam executar suas atividades sem cair em situações de *deadlock*, *data race* ou *starvation*.

Neste projeto, cada filósofo é representado por uma thread, permitindo a execução concorrente de suas atividades. A implementação rigorosa de mecanismos de sincronização, como mutexes, assegura que os garfos sejam utilizados de forma segura e ordenada. A capacidade de gerenciar a concorrência é crucial para evitar problemas como *data races*, onde múltiplas threads acessam simultaneamente os mesmos recursos, e *deadlocks*, onde threads ficam bloqueadas em espera umas pelas outras.

Como parte do currículo da 42, este projeto não apenas desenvolve habilidades técnicas em programação multithread, mas também incentiva a reflexão sobre design e arquitetura de sistemas, promovendo uma compreensão mais profunda da concorrência e seus desafios. É uma oportunidade para aprimorar tanto a lógica de programação quanto o pensamento crítico, essenciais para o desenvolvimento de software robusto e eficiente.

## Conceitos

- **Threads**: Cada filósofo é representado por uma thread, permitindo a execução concorrente das atividades de pensar, comer e dormir.
- **Data Race**: Ocorre quando dois ou mais threads acessam simultaneamente a mesma variável. A sincronização adequada é implementada para evitar esse problema.
- **Deadlock**: Acontece quando os threads ficam bloqueados, esperando uns pelos outros. Estratégias foram aplicadas para garantir uma ordem na aquisição dos garfos, evitando ciclos de espera.
- **Gerenciamento de Recursos**: Utilização de mecanismos de sincronização, como mutexes, para assegurar que os garfos sejam utilizados de maneira segura e ordenada.

## Compilação e Execução

Para compilar o projeto, utilize o seguinte comando:

```
make
```

Para executar use 

```
 ./philosophers 5 410 200 200

```

O programa recebe até 5 argumentos: 

O número de filósofos, a quantidade de tempo que pode ficar sem comer até morrer, o tempo de comer, o tempo de dormir e opcionalmente o número de refeições que os filósofos devem fazer


