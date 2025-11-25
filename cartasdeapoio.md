## TEMA 1: O CICLO DE INSTRUÇÃO (Assembly)

### CARTA 01 (Nível: Fácil)
**MISSÃO: SOMA SIMPLES**
A CPU precisa somar dois números.
1. Pegue o valor que está na memória no endereço `[100]`.
2. Pegue o valor que está na memória no endereço `[101]`.
3. Some os dois.
4. Guarde o resultado na memória no endereço `[200]`.

### CARTA 02 (Nível: Fácil)
**MISSÃO: CÓPIA DE SEGURANÇA**
Precisamos fazer um backup de um dado.
1. O valor importante está no registrador `R1`.
2. Salve esse valor na memória no endereço `[50]`.
3. Salve o mesmo valor também na memória no endereço `[51]`.

### CARTA 03 (Nível: Médio)
**MISSÃO: A TROCA (SWAP)**
Dois valores estão trocados e precisamos inverter.
* O endereço `[A]` tem o valor 10.
* O endereço `[B]` tem o valor 20.
* **Tarefa:** Escreva um código que use um registrador temporário para fazer o endereço `[A]` ficar com 20 e o `[B]` ficar com 10.

### CARTA 04 (Nível: Médio)
**MISSÃO: CÁLCULO DE IDADE**
Vamos calcular a idade baseada no ano atual.
1. O registrador `R1` tem o "Ano Atual" (ex: 2025).
2. O registrador `R2` tem o "Ano de Nascimento" (ex: 2000).
3. Subtraia o nascimento do ano atual.
4. Guarde o resultado (a idade) na memória no endereço `[300]`.

### CARTA 05 (Nível: Difícil)
**MISSÃO: EXPRESSÃO MATEMÁTICA**
Traduza a seguinte conta para Assembly: `Resultado = (X + Y) - Z`
* O valor de **X** está na memória `[10]`.
* O valor de **Y** está na memória `[11]`.
* O valor de **Z** está na memória `[12]`.
* O **Resultado** deve ser salvo na memória `[13]`.

---

## TEMA 2: LÓGICA DIGITAL (Circuitos)

### CARTA 01 (Nível: Fácil)
**MISSÃO: O INTERRUPTOR DUPLO**
Desenhe o circuito para a seguinte lógica:
"A lâmpada (S) só deve acender se o Interruptor A E o Interruptor B estiverem ligados ao mesmo tempo."
* **Expressão:** `S = A AND B`

### CARTA 02 (Nível: Fácil)
**MISSÃO: O SISTEMA DE ALARME SIMPLES**
Desenhe o circuito para a seguinte lógica:
"O alarme (S) vai disparar se o Sensor da Porta (A) for ativado OU se o Sensor da Janela (B) for ativado."
* **Expressão:** `S = A OR B`

### CARTA 03 (Nível: Médio)
**MISSÃO: A PORTA DE SEGURANÇA**
Desenhe o circuito lógico:
"A porta (S) abre se o cartão de acesso (A) for válido E a senha (B) estiver correta."

### CARTA 04 (Nível: Médio)
**MISSÃO: LÓGICA INVERTIDA**
Desenhe o circuito para a expressão: `S = NOT (A OR B)`
Explicação: A saída S só é verdadeira se nem A nem B forem verdadeiros. (Isso é uma porta NOR).

### CARTA 05 (Nível: Difícil)
**MISSÃO: O SISTEMA DE LANÇAMENTO**
Um foguete só lança (S=1) se:
1. O Computador Central (A) autorizar E...
2. (...O Engenheiro Chefe (B) apertar o botão OU o Comandante (C) apertar o botão).
* **Expressão:** `S = A AND (B OR C)`

---

## TEMA 3: ENTRADA E SAÍDA (Periféricos)

### CARTA 01 (Nível: Fácil)
**MISSÃO: POLLING (A PERGUNTA CHATA)**
Desenhe um Fluxograma simples onde a CPU fica presa em um loop perguntando:
"Impressora, você está pronta?"
* Se a resposta for NÃO -> Volta a perguntar.
* Se a resposta for SIM -> Envia o dado.

### CARTA 02 (Nível: Fácil)
**MISSÃO: INTERRUPÇÃO (O AVISO)**
Desenhe um Fluxograma que mostre:
1. A CPU está trabalhando feliz em um cálculo.
2. O Teclado manda um sinal de "Interrupção" (o usuário apertou uma tecla).
3. A CPU para o cálculo.
4. A CPU atende o teclado (lê a tecla).
5. A CPU volta para o cálculo de onde parou.

### CARTA 03 (Nível: Médio)
**MISSÃO: O CONTROLADOR DE VÍDEO**
Desenhe o esquema de conexão:
Mostre como a CPU envia dados para a Memória de Vídeo, e como o Monitor lê esses dados da memória para mostrar a imagem.

### CARTA 04 (Nível: Médio)
**MISSÃO: DMA (O AJUDANTE RÁPIDO)**
Desenhe um Fluxograma da transferência via DMA:
1. CPU ordena ao DMA: "Copie dados do Disco para a RAM".
2. CPU vai fazer outra coisa (fica livre).
3. DMA transfere os dados sozinho.
4. Quando termina, DMA avisa a CPU com uma Interrupção.

### CARTA 05 (Nível: Difícil)
**MISSÃO: BUFFER DE TECLADO**
Desenhe uma situação onde a CPU está muito ocupada:
1. O usuário digita rápido: "A", "B", "C".
2. A CPU não consegue ler na hora.
3. Mostre os caracteres entrando em uma "Fila" (Buffer) dentro do controlador do teclado.
4. Depois, a CPU lê "A", depois "B", depois "C" dessa fila.
