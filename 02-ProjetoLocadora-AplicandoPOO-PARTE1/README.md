## PROJETO: Locadora de Veículos (versão orientada a objetos)

Este projeto é uma aplicação de exemplo em Java que simula um sistema simples de locadora de veículos. Ao contrário da versão procedural anterior, esta implementação usa orientação a objetos com as classes `Carro`, `Locadora` e `Main`.

**Arquivos principais**

- `src/Carro.java` — modelo de domínio que representa um carro (modelo, marca, preço da diária, seguro, disponibilidade e tipo) e contém lógica relacionada (alugar, devolver, cálculo do valor total).
- `src/Locadora.java` — classe que mantém um array de `Carro` e implementa operações da locadora: listar, buscar por modelo, alugar, devolver e buscar por tipo.
- `src/Main.java` — ponto de entrada com interface de linha de comando (menu) para interagir com a `Locadora`.
- `bin/` — classes compiladas (.class) geradas previamente.

**Funcionalidades**

- Listar todos os veículos.
- Listar veículos disponíveis.
- Alugar um veículo (selecionar por modelo e informar dias) — imprime o valor total.
- Devolver um veículo.
- Buscar veículos por tipo (ex.: hatch, caminhhonete).

**Observações e limitações atuais**

- Não há persistência: os dados (lista de carros e disponibilidade) são reinicializados a cada execução.
- Entrada de usuário assume formatos simples (uso de `Scanner.next()`); entradas inválidas podem causar comportamento inesperado.
- A busca e seleção de carros é feita por modelo (string), não por um ID numérico.
