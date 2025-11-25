# Conjunto de Instruções (ISA) Padrão para o Jogo

> **Regra:** Use apenas estes comandos para traduzir as tarefas.

## Comandos Disponíveis

| Comando | Sintaxe | Descrição |
| :--- | :--- | :--- |
| **LOAD** | `LOAD Rx, [End]` | Carrega o valor da memória `[End]` para o registrador `Rx`. |
| **STORE** | `STORE Rx, [End]` | Salva o valor de `Rx` na memória no endereço `[End]`. |
| **ADD** | `ADD Rx, Ry, Rz` | Soma `Ry` + `Rz` e guarda o resultado em `Rx`. |
| **SUB** | `SUB Rx, Ry, Rz` | Subtrai `Ry` - `Rz` e guarda o resultado em `Rx`. |
| **MOV** | `MOV Rx, Ry` | Copia o valor de `Ry` para `Rx`. |
| **JUMP** | `JUMP [End]` | Pula para a linha de código no endereço `[End]`. |

## Definições
* **Rx, Ry, Rz**: São registradores numéricos (ex: `R1`, `R2`, `R3`...).
* **[End]**: Representa um endereço de memória ou rótulo de linha.
