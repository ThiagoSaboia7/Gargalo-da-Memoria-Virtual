# Parecer Técnico: Diagnóstico de Infraestrutura – O Gargalo da Memória Virtual

 
*Autores:* [Thiago saboia](https://github.com/ThiagoSaboia7) --- [João Victor](https://github.com/Joao-Victorx)

## Introdução

O presente documento apresenta o parecer técnico referente ao diagnóstico de desempenho do servidor de banco de dados da empresa TechBuy durante os eventos de alta temporada. O cenário monitorado indica alto uso de disco rígido ($100\%$ de I/O), processador ocioso em termos de regras de negócio e frequentes trocas de contexto. A análise a seguir detalha os conceitos de gerenciamento de memória virtual, paginação por demanda, o papel crítico da TLB e os impactos operacionais decorrentes.
