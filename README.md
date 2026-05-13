# IoT ESP32 - Robô Explorador Espacial

## Descrição do Projeto

Este projeto faz parte de uma atividade prática de Internet das Coisas (IoT) utilizando ESP32, simulação no Wokwi e integração com controle remoto.

O objetivo é simular um robô explorador espacial capaz de procurar indícios de vida extraterrestre em um planeta fictício. O sistema utiliza um ESP32 como controle remoto no Wokwi e outro ESP32 físico como robô explorador.

Nesta etapa do projeto foi desenvolvido o controle remoto virtual utilizando:

* ESP32
* Joystick analógico
* LEDs indicadores
* Botão de desligamento remoto

O controle remoto envia comandos de movimentação para o robô e informa o status da comunicação através dos LEDs e do Monitor Serial.

---

# Objetivo da Etapa

Desenvolver um sistema de controle remoto com ESP32 no Wokwi capaz de:

* Ler os movimentos de um joystick analógico
* Enviar comandos de movimentação:

  * Frente
  * Trás
  * Esquerda
  * Direita
* Simular o desligamento remoto do robô
* Exibir os comandos no Monitor Serial
* Indicar o estado da conexão utilizando LEDs

---

# Componentes Utilizados

* 1x ESP32 DevKit V4
* 1x Joystick Analógico
* 1x LED Verde
* 1x LED Vermelho
* 2x Resistores 220Ω
* 1x Botão Push Button
* Jumpers virtuais do Wokwi

---

# Funcionamento do Sistema

## Controle de Movimentação

O joystick analógico controla as direções do robô:

| Movimento do Joystick | Comando              |
| --------------------- | -------------------- |
| Frente                | Motores para frente  |
| Trás                  | Motores para trás    |
| Esquerda              | Motor direito ativo  |
| Direita               | Motor esquerdo ativo |

Os comandos são exibidos continuamente no Monitor Serial.

---

## Botão de Desligamento

Ao pressionar o botão:

* O sistema envia o comando:

```text
DESLIGAR
```

* O robô para imediatamente
* O LED vermelho acende
* O LED verde apaga
* O Monitor Serial exibe mensagens de desligamento

---

## LEDs Indicadores

| LED      | Significado                    |
| -------- | ------------------------------ |
| Verde    | Robô ligado e conectado        |
| Vermelho | Robô desligado ou desconectado |

---

# Monitor Serial

O Monitor Serial exibe:

* Direção enviada
* Valores dos eixos X e Y do joystick
* Estado atual do robô
* Mensagem de desligamento remoto

Exemplo:

```text
Comando: Frente
X: 2048 | Y: 4095
Status: Robô ligado
```

---

# Como Executar no Wokwi

1. Acesse o link do projeto no Wokwi:

https://wokwi.com/projects/463932769161369601

2. Clique em "Start Simulation"

3. Utilize o joystick virtual para controlar o robô

4. Pressione o botão por 1 segundo para simular o desligamento remoto

5. Abra o Monitor Serial para visualizar os comandos enviados

---

# Tecnologias Utilizadas

* ESP32
* Arduino Framework
* Wokwi Simulator
* C/C++ para Arduino
* GitHub
