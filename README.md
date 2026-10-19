# Cálculo de Salário

Aplicação de console em Java que calcula a renda mensal de um funcionário a partir dos contratos por hora cadastrados para ele.

O usuário informa os dados do departamento e do funcionário, cadastra quantos contratos quiser e, no final, escolhe um mês e um ano para ver o total recebido naquele período.

## Funcionalidades

- Cadastro de departamento e funcionário (nome, nível e salário base)
- Cadastro de vários contratos por funcionário (data, valor por hora e duração em horas)
- Cálculo da renda de um mês/ano específico (salário base + contratos do período)
- Exibição do nome, do departamento e da renda calculada

## Tecnologias e recursos utilizados

- **Java** (JDK 21 ou superior)
- **IntelliJ IDEA** como IDE
- **Git e GitHub** para versionamento

### Conceitos de programação aplicados

- Programação Orientada a Objetos (classes, atributos, métodos, construtores, getters e setters)
- Composição e associação entre objetos (`Worker` possui um `Department` e uma lista de `HourContract`)
- Enumerações (`enum WorkerLevel`)
- Listas (`List` / `ArrayList`)
- Manipulação de datas com `Date`, `SimpleDateFormat` e `Calendar`
- Tratamento de exceções (`ParseException`)
- Leitura de dados pelo console com `Scanner`
- Formatação de saída com `String.format` e `Locale`

## Estrutura do projeto

```
src/
├── Application/
│   └── program.java         # Classe principal (entrada e saída de dados)
└── entities/
    ├── Department.java     # Departamento do funcionário
    ├── HourContract.java   # Contrato por hora
    ├── Worker.java         # Funcionário e cálculo da renda
    └── enums/
        └── WorkerLevel.java # Níveis do funcionário
```

## Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/yokohamacaio62-afk/calculo-de-salario.git
   ```
2. Abra o projeto no IntelliJ IDEA (ou outra IDE Java).
3. Execute a classe `program` (pacote `Application`).

## Exemplo de uso

```
Enter departament name: Design
Enter worker data:
Name: Alex
Level: MID_LEVEL
Base salary: 1200.00
How many contracts to this worker? 3
Enter contract #1 data: Date (DD/MM/YYYY): 20/08/2018
Value per hour: 50.00
Duration (hours): 20
Enter contract #2 data: Date (DD/MM/YYYY): 13/06/2018
Value per hour: 30.00
Duration (hours): 18
Enter contract #3 data: Date (DD/MM/YYYY): 25/08/2018
Value per hour: 80.00
Duration (hours): 10

Enter month and year to calculate income (MM/YYYY): 08/2018
Name: Alex
Department: Design
Income for 08/2018: 3000.00
```

> **Atenção:** o nível do funcionário deve ser digitado exatamente como definido no enum (por exemplo `JUNIOR`, `MID_LEVEL` ou `SENIOR`), e o mês/ano deve seguir o formato `MM/YYYY`.
