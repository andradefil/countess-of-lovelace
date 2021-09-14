Pinos de entrada e saida
Consigo ler de pinos de entrada e saída e trigar resultados, interfacear o microcontrolador com outros dispositivos, sejam dispositivos de entrada ou saída.
- Niveis de tensão 
- Outras características (Estudos dos periféricos)

Microcontrolador ATMEGA 328
Inicia o estudo de periféricos 

Dispositivos de I/O e interrupções
Clock - Oscilador interno, ou cristal de alta frequência externo
Memórias -> Flash, RAM e EEPROM


Dispositivos de entrada e saída (Pinos programáveis, pode ser programado para ser de entrada ou saída, exceto pinos Vcc e Gnd e VAnalog e pinos de cristal de clock)
- Realizam a interface do controlador com o "Mundo externo"
- Presentes em praticamente todos os pinos
- Função de saída: Latches.
- Entradas: buffers com saídas tri-state
- Configurações das portas feita por meio de **registradores** (endereços de memória, 2 tipos:
	 - Proposito geral: Armazena informação temporária durante a execução
	 - Proposito específico: Altera fisicamente o comportamento do microcontrolador
	 - 3 registradores por pino: entrada ou saida, lê o estado da entrada, colocar o estado caso seja saída)

Circuito esquemático geral das portas de I/O do Atmega 328
![[Screen Shot 2021-09-13 at 20.46.03.png]]

Características elétricas (Tudo é a base de eletricidade)
![[Screen Shot 2021-09-13 at 21.05.01.png]]

Consumo vs Frequência
![[Screen Shot 2021-09-13 at 21.06.43.png]]


Interrupções
Em um projeto clássico de software de sistemas microcontrolados, é implementado um laço infinito dentro da função principal.
![[Screen Shot 2021-09-13 at 21.09.40.png]]
A interrupção recebe um "evento" é gerado uma interrupção, o programa pausa a função aonde estiver, e ativa a função de interrupção, depois da execução da função de interrupção o fluxo de execução é retomado para pela função princípal.

Exemplos:
 - Temporaziadores: Interrupçòes por término na contagem de intervalo de tempo
 - Conversor analógico / digital: interrupção ao termino do processo de conversão.
 - Portas de I/O: Interrupção por mudança no sinal lógico em um dos pinos externos.
 
 Interrupções externas
-  Sào interrupções atreladas a mudança de estado de um pino;
 - Necessário configurar os pinos como entrada;
 - Necessário habilitar a interrupção no registrador **específico do pino**
- Configurações mais refinadas para o PD2 e PD3 do ATmega328.