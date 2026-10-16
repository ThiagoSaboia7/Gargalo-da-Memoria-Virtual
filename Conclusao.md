## Conclusão

A lentidão da TechBuy é thrashing: a RAM não comporta os working sets dos processos na alta temporada, os Page Faults se multiplicam, o disco satura e a CPU fica parada esperando. As trocas de contexto frequentes esvaziam a TLB e pioram o tempo de acesso. Dobrar a RAM resolve a causa principal, e o resultado é mais durável se vier junto com o controle da carga.
