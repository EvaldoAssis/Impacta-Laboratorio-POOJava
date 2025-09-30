## PROJETO: Locadora de Veículos (código procedural)

Este projeto é uma aplicação de exemplo em Java, codificada em estilo procedural, que simula um sistema simples de locadora de veículos.

Objetivo

- Fornecer um exemplo didático de como organizar um programa Java pequeno em formato procedural.
- Demonstrar operações básicas de um sistema de locação: listar veículos, listar disponíveis, alugar, devolver e buscar por tipo.

Descrição do código

- O ponto de entrada é o arquivo `src/Main.java`.
- Os dados dos veículos são mantidos em arrays estáticos paralelos (`modelos`, `tipos`, `precosDiaria`, `disponibilidade`, `locatarios`).
- A interface é por linha de comando (terminal) e apresenta um menu com opções numeradas.

Funcionalidades implementadas

- Listar todos os veículos com status e locatário (se houver).
- Listar apenas veículos disponíveis.
- Alugar um veículo: escolher por ID, informar nome do locatário e quantidade de dias; atualiza disponibilidade e locatário.
- Devolver um veículo: escolher por ID entre os alugados; reseta disponibilidade e locatário.
- Buscar veículos por tipo (ex.: Sedan, SUV, Hatch).

Limitações

- Estrutura procedural com dados em arrays paralelos — não é orientado a objetos.
- Sem persistência: todos os dados são voláteis e reiniciam ao executar o programa novamente.
- Validações e tratamento de entradas são mínimos (ex.: entradas inválidas podem encerrar fluxos ou retornar ao menu).
