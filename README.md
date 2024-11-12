### ReadMe.md

# Sistema de Segurança Pessoal (SSP) - VHDL

## Descrição

O **Sistema de Segurança Pessoal (SSP)** é um projeto desenvolvido em **VHDL** que implementa uma **Máquina de Estados Finita (FSM)** para monitorar a presença de pessoas. Quando detectada a presença de alguém, o sistema desativa o motor e ativa um alarme sonoro e visual.

## 🛠️ **Funcionamento do Sistema**

## Estados do Sistema

1. **Inicial (INITIAL):**  
   - LED verde ligado, motor e alarme desligados.  
   - Aguardando o botão de iniciar (`pinRun`).

2. **Execução (RUN):**  
   - Motor e LED amarelo ligados.  
   - Monitora presença de pessoas.

3. **Alarme (FAULT):**  
   - LED vermelho e buzzer ligados, motor desligado.  
   - Aguarda reconhecimento do alarme através do botão de reset (`pinReset`).

4. **Reset (RESET):**  
   - Retorna ao estado inicial após uma detecção de presença.

## Entradas e Saídas

**Entradas:**  
- `clk`: Clock do sistema.  
- `pinSensor`: Detecta presença de pessoas.  
- `pinRun`: Botão de início.  
- `pinReset`: Botão de reset.

**Saídas:**  
- `pinMotor`: Controle do motor.  
- `pinBuzzer`: Controle do buzzer.  
- `pinledVerde`: LED verde (sistema pronto).  
- `pinledAmarelo`: LED amarelo (sistema em execução).  
- `pinledVermelho`: LED vermelho (alarme ativado).

## Uso

1. Compile o código no **Quartus Prime**.  
2. Realize simulações usando **ModelSim** ou o simulador do Quartus.  
3. Implemente o projeto em uma FPGA e conecte sensores, LEDs, motor e buzzer para testes em hardware.
