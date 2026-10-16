## Parte A: O Fenômeno da Paginação e o Gargalo do Disco

### 1. O que é uma "Falta de Página" (Page Fault)?

No modelo de *Memória Virtual, o espaço de endereçamento lógico de um processo é dividido em blocos de tamanho fixo chamados **páginas, enquanto a memória física (RAM) é dividida em blocos equivalentes chamados **molduras (*frames)**.

Um *Page Fault* (falta de página) ocorre quando o processador (via MMU - Memory Management Unit) tenta traduzir um endereço virtual para um endereço físico e constata que a página referenciada não se encontra carregada na memória principal RAM (indicado pelo bit de presença/ausência igual a zero na tabela de páginas).

* Quando isso acontece, o hardware gera uma interrupção (trap), suspendendo temporariamente a instrução atual.
* O Sistema Operacional intervém, localiza a página correspondente no dispositivo de armazenamento secundário (disco/swap), aloca um frame livre na RAM e realiza a transferência dos dados do disco para a memória principal.
