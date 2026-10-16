## Parte C: Síntese e Solução

### 1. Qual o efeito de dobrar a RAM?

Se a causa é falta de memória, como os sintomas indicam, dobrar a RAM deve reduzir bastante os Page Faults e o uso do disco.

Na memória virtual, apenas o working set de cada processo (as páginas que ele usa ativamente no momento) precisa estar na RAM. O resto fica no disco. A taxa de Page Faults depende de quantos frames o processo tem em relação ao seu working set. Se o working set cabe na memória, as faltas ocorrem principalmente quando o processo muda de fase. Se não cabe, as faltas são contínuas (Tanenbaum).

Com o dobro de frames, mais working sets cabem na RAM. Há menos substituições, menos páginas modificadas gravadas no disco e menos leituras repetidas. A fila do disco diminui, os processos voltam a rodar com fluidez.
