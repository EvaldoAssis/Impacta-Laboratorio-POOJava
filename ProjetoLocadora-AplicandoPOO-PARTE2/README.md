## PROJETO: Locadora de Veículos (versão orientada a objetos com herança, polimorfismo e interface)

Este repositório contém uma aplicação em Java que modela uma locadora de veículos usando conceitos de orientação a objetos.

O código fonte está em `src/` e as classes compiladas estão em `bin/` (fornecidas). A implementação atual apresenta uma hierarquia simples de veículos e duas implementações básicas de um "banco de dados" em memória.

Arquivos principais (src/):

- `Veiculo.java` — classe abstrata/base que define atributos e comportamento comuns a todos os veículos (modelo, marca, preço da diária, seguro, disponibilidade, tipo e operações básicas).
- `Carro.java` — subclasse de `Veiculo` com comportamento específico (quando aplicável).
- `Moto.java` — subclasse de `Veiculo` para motos.
- `Locadora.java` — gerencia a coleção de veículos e providencia operações: listar, buscar por modelo, alugar, devolver e buscar por tipo.
- `BancoDeDados.java` — interface/abstração (ou classe base) para armazenamento de veículos.
- `BancoDeDadosEmMemoria.java` — implementação que mantém os veículos em memória.
- `BancoDeDadosEmMemoriaPremium.java` — variação da implementação em memória (ex.: com comportamento ou conjunto de dados diferente).
- `Main.java` — ponto de entrada com um menu de console para interação com a `Locadora`.

**Funcionalidades disponíveis:**

- Listar todos os veículos cadastrados.
- Listar veículos disponíveis para locação.
- Buscar veículo por modelo (busca por string).
- Alugar um veículo (informa modelo e número de dias) — imprime o valor total do aluguel.
- Devolver um veículo (marca como disponível novamente).

**Observações e limitações importantes:**

- Persistência: atualmente não há persistência em disco; todas as informações são reiniciadas a cada execução (implementação em memória).
- Identificação: a seleção/consulta é feita por modelo (string) — não há ID numérico único para cada veículo.
- Validação de entrada: a interface de console usa entradas simples; entradas inválidas podem causar comportamento inesperado.

**Resumo das responsabilidades (rápido):**

- Modelos: `Veiculo`, `Carro`, `Moto` — representam dados e regras do veículo.
- Persistência/DB: `BancoDeDados*` — abstração e implementações em memória.
- Serviço: `Locadora` — lógica de negócio e operações da locadora.
- CLI: `Main` — interação via terminal.
