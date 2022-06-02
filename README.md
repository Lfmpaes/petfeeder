
PetFeeder
=========
Um alimentador para pets baseado em Arduino e Raspberry Pi. Este repositório agrupa o fluxo utilizado no Node-RED para a conexão com o sensor e o atuador, além da conexão via internet através do protocolo MQTT.


### Materiais Utilizados

 - Raspberry Pi Model 3B+
 - Arduino Uno
 - Servo Motor 9g (SG90)
 - Sensor Ultrassônico HC-SR04
 - Node-RED
 - Protoboard
 - Jumpers
 - 3x Resistores 1k Ω ***ou*** 1 Resistor 1k Ω + 1 Resistor 2k Ω

### Bibliotecas Node-RED
Para habilitar mais funcionalidades no Node-RED, foram instalados os seguintes pacotes.

 - *node-red-contrib-loop-processing*: gerenciamento de fluxos de loop
 - *node-red-dashboard*: um dashboard customizável
 - *node-red-node-arduino*: possibilita a comunicação com o Arduino através do protocolo Firmata
 - *node-red-node-pi-gpio*: possibilita a comunicação com os pinos GPIO do Raspberry Pi
 - *node-red-node-pisrf*: Fornece um node para leitura de dados do sensor HC-SR04

## Montagem da Solução

![Conexão dos dispositivos físicos](https://i.imgur.com/mrTsSPZ.png)

 - [ ] Faça uma ligação dos pinos 5V e GND do Arduino respectivamente nas linhas + e - da Protoboard.
 - [ ] Conecte os fios do Servo na seguinte ordem: *fio marrom* no GND, *fio vermelho* no 5V, e o *fio laranja* na porta digital 8 do Arduino.
 - [ ] Faça as ligações de energia do sensor HC-SR04 ao Arduino: pino Gnd ao GND do Arduino, e pino Vcc ao 5V do Arduino.
 - [ ] Conecte o pino Trig do HC-SR04 ao pino GPIO 7 do Raspberry Pi.
 - [ ] Faça um divisor de voltagem para conectar o pino Echo do HC-SR04. Insira um resistor de 2k Ω (ou dois resistores de 1k Ω) entre o pino Echo e outra linha da Protoboard. Mais abaixo, na mesma linha, conecte um resistor de 1k Ω à linha GND da Protoboard. Entre essas duas conexões, faça uma ligação entre o ponto e o pino GPIO 11 do Raspberry Pi. 
 

> Para mais detalhes acerca da organização do divisor de voltagem e a conexão do HC-SR04 com o Raspberry Pi, confira [neste link](https://pimylifeup.com/raspberry-pi-distance-sensor/).

 - [ ] Instale as bibliotecas do Node-RED e importe o projeto.
 - [ ] Atualize os nós de conexão MQTT para seus tópicos de escolha.

## Sobre o Projeto
Este foi um projeto realizado por Luiz Fernando Menezes Paes para a disciplina de Objetos Inteligentes Conectados, no curso de Sistemas de Informação da Universidade Presbiteriana Mackenzie / SP.

Entre em contato comigo em todas as redes sociais pelo @Lfmpaes.
