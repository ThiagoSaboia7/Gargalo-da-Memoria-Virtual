## Parte B: A TLB

### 1. O que é a TLB e por que ela fica em hardware?

A *TLB* (Translation Lookaside Buffer) é uma pequena memória cache, localizada na MMU, que guarda as traduções de página virtual para frame usadas mais recentemente. Sem ela, todo acesso à memória exigiria antes um acesso à tabela de páginas na RAM, e o tempo de acesso dobraria (Silberschatz). Ela funciona porque os programas acessam poucas páginas com muita frequência (localidade de referência).

Ela é implementada em hardware por motivos fundamentais:
* *Frequência de Acesso:* A tradução ocorre em todo acesso à memória, inclusive na busca de instruções. Se a TLB estivesse na RAM, o ganho de velocidade se perderia.
* *Busca Associativa:* O número da página é comparado com todas as entradas ao mesmo tempo. A RAM comum é acessada por endereço, enquanto a TLB realiza busca paralela por conteúdo (associativa).
