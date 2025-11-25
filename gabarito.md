# Gabarito Oficial - Telefone sem Fio AOC

> **Nota:** Este documento contém as respostas esperadas para a rodada de cada carta. Use-o na fase de correção para validar se o grupo saiu pelo caminho certo.

## TEMA 1: O CICLO DE INSTRUÇÃO (Assembly)

### CARTA 01 (Soma Simples)
**Solução Esperada:**
LOAD R1, 100    ; Carrega valor do endereço 100
LOAD R2, 101    ; Carrega valor do endereço 101
ADD R3, R1, R2  ; Soma os dois
STORE R3, 200   ; Salva no endereço 200

### CARTA 02 (Cópia de Segurança)
**Solução Esperada:**
STORE R1, 50    ; Salva R1 no primeiro endereço
STORE R1, 51    ; Salva R1 no segundo endereço

### CARTA 03 (A Troca / Swap)
**Solução Esperada:**
LOAD R1, A      ; R1 pega valor de A (10)
LOAD R2, B      ; R2 pega valor de B (20)
STORE R2, A     ; A recebe valor de R2 (20)
STORE R1, B     ; B recebe valor de R1 (10)

### CARTA 04 (Cálculo de Idade)
**Solução Esperada:**
SUB R3, R1, R2  ; R3 = Ano Atual (R1) - Ano Nasc (R2)
STORE R3, 300   ; Salva a idade na memória 300

### CARTA 05 (Expressão Matemática)
* **Expressão:** `(X + Y) - Z`
**Solução Esperada:**
LOAD R1, 10     ; Carrega X
LOAD R2, 11     ; Carrega Y
LOAD R3, 12     ; Carrega Z
ADD R4, R1, R2  ; R4 = X + Y
SUB R5, R4, R3  ; R5 = Resultado - Z
STORE R5, 13    ; Salva o final

## TEMA 2: LÓGICA DIGITAL (Circuitos)

### CARTA 01 (Interruptor Duplo)
* **Expressão:** `S = A AND B`
* **Desenho Correto:** Uma porta lógica **AND** (formato de "D") com duas pernas de entrada (A, B) e uma saída (S).

### CARTA 02 (Alarme Simples)
* **Expressão:** `S = A OR B`
* **Desenho Correto:** Uma porta lógica **OR** (formato de ponta de flecha curva) com duas entradas (A, B) e uma saída (S).

### CARTA 03 (Porta de Segurança)
* **Lógica:** Cartão Válido **E** Senha Correta.
* **Desenho Correto:** Igual à Carta 01, uma porta **AND**. Ambas as condições precisam ser verdadeiras para a porta abrir.

### CARTA 04 (Lógica Invertida)
* **Expressão:** `S = NOT (A OR B)`
* **Desenho Correto:** Uma porta **NOR**.
    1. Desenha-se uma porta **OR** normal.
    2. Adiciona-se uma "bolinha" (círculo pequeno) na ponta da saída. Essa bolinha representa o "NOT" (inversão).

### CARTA 05 (Sistema de Lançamento)
* **Expressão:** `S = A AND (B OR C)`
* **Desenho Correto:** Um circuito composto.
    1. Primeiro, uma porta **OR** que recebe as entradas B e C.
    2. A saída dessa porta OR entra em uma porta **AND**.
    3. A outra entrada dessa porta AND recebe o sinal A.

## TEMA 3: ENTRADA E SAÍDA (Periféricos)

### CARTA 01 (Polling)
**Fluxograma Correto:**
Deve mostrar um ciclo fechado (loop):
1. Caixa de Decisão (Losango): "Impressora Pronta?"
2. Seta "NÃO": Volta para antes da pergunta (loop).
3. Seta "SIM": Segue para a caixa "Enviar Dado".

### CARTA 02 (Interrupção)
**Fluxograma Correto:**
Deve mostrar uma linha do tempo quebrada:
1. Bloco "Processamento Normal".
2. Seta saindo para o lado: "Sinal de Interrupção".
3. Bloco "Tratar Teclado".
4. Seta voltando **exatamente** para onde parou no "Processamento Normal".

### CARTA 03 (Controlador de Vídeo)
**Esquema Correto:**
* **Fluxo dos dados:** CPU -> (escreve em) -> **Memória de Vídeo** -> (é lida por) -> Monitor/Vídeo.
* *Nota:* O erro comum é ligar a CPU direto no Monitor. A resposta certa precisa ter a memória no meio.

### CARTA 04 (DMA)
**Fluxograma Correto:**
1. CPU configura DMA (diz "copie X para Y").
2. Caminhos se dividem (**Paralelismo**):
    * Caminho A: CPU faz outras tarefas.
    * Caminho B: DMA transfere dados Disco -> RAM.
3. Caminhos se juntam: DMA envia Interrupção "Terminei" para a CPU.

### CARTA 05 (Buffer de Teclado)
**Esquema Correto:**
Deve ilustrar uma estrutura de fila (FIFO - First In, First Out):
1. Teclas 'A', 'B', 'C' entrando em uma caixa/lista.
2. Elas ficam armazenadas temporariamente.
3. A CPU retira 'A', depois 'B', depois 'C' na mesma ordem, mesmo que com atraso.
