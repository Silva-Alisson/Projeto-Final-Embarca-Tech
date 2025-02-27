# Sistema de Segurança Residencial Acessível

## Visão Geral
Este projeto visa oferecer uma solução acessível para segurança residencial, utilizando o microcontrolador Raspberry Pi Pico W e a biblioteca BitdogLab. O objetivo é criar um sistema modular, de baixo custo e independente de infraestrutura complexa, permitindo que qualquer pessoa possa implementá-lo sem necessitar de serviços ou contratos caros.

## Componentes Utilizados
- **Raspberry Pi Pico W**: Microcontrolador principal do sistema.
- **BitdogLab**: Biblioteca utilizada para o gerenciamento dos periféricos.
- **Display OLED (I2C)**: Responsável pela exibição do status do sistema.
- **Botões GPIO**: Simulam sensores de segurança.
- **Comunicação UART**: Possibilidade de expansão para envio de alertas a dispositivos externos.

## Funcionamento do Sistema
O sistema opera em dois modos:

1. **Modo Ativo**: 
   - Monitora os eventos nos botões GPIO.
   - Exibe alertas no display OLED.
   - Possibilita, via UART, o envio de mensagens para dispositivos externos (como módulos GSM para envio de SMS).

2. **Modo Inativo**:
   - O sistema entra em repouso, suspendendo os alertas e a comunicação externa.
   - O status "inativo" é exibido no display OLED.

A alternância entre os modos é realizada por um botão físico conectado ao GPIO, e o status é atualizado em tempo real no display.

## Como Rodar o Projeto
1. **Configuração do Hardware**:
   - Conecte o display OLED ao Raspberry Pi Pico W via interface I2C (SDA no GPIO14 e SCL no GPIO15).
   - Conecte os botões GPIO (por exemplo, GPIO5 e GPIO6 para simular sensores e GPIO22 para alternar entre os modos).

2. **Configuração do Software**:
   - Instale a biblioteca BitdogLab.
   - Compile e carregue o firmware no Raspberry Pi Pico W conforme as instruções da BitdogLab.

3. **Execução**:
   - Utilize a plataforma BitdogLab para gerenciar os pinos e monitorar os eventos.
   - Acompanhe os alertas e o status do sistema no display OLED.

## Conclusão
Este projeto proporciona uma solução de segurança residencial eficaz e de baixo custo, permitindo que usuários implementem um sistema confiável sem a necessidade de investimentos altos ou contratos recorrentes. Com a possibilidade de futuras expansões, como a integração com módulos de comunicação para envio de alertas remotos, o sistema se adapta às necessidades de diferentes usuários, democratizando o acesso à tecnologia de monitoramento.
