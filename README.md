# Projeto: Controle de LEDs RGB e Display SSD1306 com Joystick

Este projeto tem como objetivo o controle de LEDs RGB e um display SSD1306 utilizando um joystick analógico com a placa BitDogLab, baseada no microcontrolador RP2040. Através do joystick, será possível controlar a intensidade dos LEDs e mover um quadrado no display, com funcionalidades adicionais associadas a botões.

## Objetivos do Projeto

- Compreender o funcionamento do conversor analógico-digital (ADC) no RP2040.
- Utilizar PWM para controlar a intensidade dos LEDs RGB com base nos valores do joystick.
- Representar a posição do joystick em um display SSD1306 por meio de um quadrado móvel.
- Aplicar o protocolo de comunicação I2C para integração com o display.

## Funcionalidades

### LEDs RGB
- **LED Azul**: Controlado pelo eixo Y do joystick. O brilho aumenta conforme o movimento do joystick para cima ou para baixo.
- **LED Vermelho**: Controlado pelo eixo X do joystick. O brilho aumenta conforme o movimento do joystick para a esquerda ou direita.
- Os LEDs são controlados via PWM, permitindo variação suave de intensidade.

### Display SSD1306
- Um quadrado de 8x8 pixels será exibido no display e se moverá proporcionalmente aos valores capturados pelo joystick.

### Botões do Joystick
- **Botão do Joystick**: Alterna o estado do LED verde e altera o estilo da borda do display a cada acionamento.
- **Botão A**: Ativa ou desativa os LEDs PWM a cada acionamento.

## Requisitos de Hardware

- **Placa BitDogLab** com:
  - LED RGB conectado aos pinos GPIO 11, 12 e 13.
  - Botão do Joystick na GPIO 22.
  - Joystick nos pinos GPIO 26 e 27.
  - Botão A na GPIO 5.
  - Display SSD1306 via I2C (GPIO 14 e GPIO 15).

## Requisitos do Projeto

1. **Uso de interrupções**: Todas as funcionalidades dos botões devem ser implementadas usando interrupções (IRQ).
2. **Debouncing**: Implementação do tratamento de debounce dos botões via software.
3. **Uso do Display 128x64**: Implementação do protocolo I2C para controle do display e visualização do quadrado.
4. **Organização do código**: O código deve ser bem estruturado, comentado e fácil de entender.

## Instruções de Uso

1. Clone o repositório para sua máquina:
    ```bash
    git clone https://github.com/KaianS/Conversores-A-D.git
    ```
2. Conecte a placa BitDogLab.
3. Compile e carregue o código no seu RP2040.
4. Execute o código e movimente o joystick para interagir com os LEDs e o display.

## Como Contribuir

1. Faça um fork do repositório.
2. Crie uma branch para sua feature (`git checkout -b minha-feature`).
3. Faça commit das suas alterações (`git commit -am 'Adiciona nova feature'`).
4. Envie a branch para o repositório remoto (`git push origin minha-feature`).
5. Abra um pull request.

## Vídeo de Demonstração

[![Watch the video](https://img.youtube.com/vi/zy5xyYdlbWk/maxresdefault.jpg)](https://youtu.be/zy5xyYdlbWk)

### [Assista aqui o vídeo](https://youtu.be/zy5xyYdlbWk)

## Considerações Finais

Este projeto serve como uma excelente oportunidade para consolidar conhecimentos sobre programação de microcontroladores, controle de LEDs via PWM, manipulação de hardware e uso do protocolo I2C.
