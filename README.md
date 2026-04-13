## ℹ️ Sobre o GRBL

**GRBL** é um firmware de código aberto altamente otimizado, escrito em C, que oferece controle de movimento CNC de alta performance com baixo custo. Funciona nativamente em placas Arduino com processador ATmega328.

### Características Principais do GRBL:

- **Alto Desempenho**: Mantém até 30kHz de pulsos de controle estáveis e sem jitter
- **G-code Padrão**: Aceita código G padrão compatível com ferramentas CAM profissionais
- **Gestão de Aceleração**: Look-ahead inteligente até 18 movimentos à frente para aceleração suave sem sobressaltos
- **Suporta**: Arcos, círculos, movimento helicoidal e todos os principais comandos G-code
- **Software Livre**: Licença GPLv3

### Versão Instalada:

Este projeto utiliza **GRBL v0.9j ou superior**, com as seguintes características:

- **Baudrate**: 115200 bps
- **Processador**: ATmega328 (Arduino Uno)
- **Controle Variável**: Suporte a velocidade variável e controle PWM para o laser
- **Homing Automático**: Ciclo de homing baseado em switches de fim de curso

### Comandos G-code Suportados:

**Comandos Não-Modais**: G4, G10L2, G10L20, G28, G30, G28.1, G30.1, G53, G92, G92.1

**Modos de Movimento**: G0, G1, G2, G3, G38.2, G38.3, G38.4, G38.5, G80

**Modos de Taxa de Avanço**: G93, G94

**Modos de Unidade**: G20, G21

**Controle de Laser**: M3 (ligar), M4 (variável), M5 (desligar)

**Controle de Movimento**: F (velocidade), X, Y, Z, S (velocidade do laser)

***
### Passos de Instalação:

1. **Clonar/Baixar o firmware GRBL**
   ```
   git clone https://github.com/gnea/grbl.git
   cd grbl/grbl
   ```

2. **Configurar para o seu hardware** (editar `config.h` ou usar `defaults.h`)
   - Selecionar a configuração correta para sua máquina
   - Ajustar corrente dos motores
   - Definir limites de movimento

3. **Compilar e fazer upload**
   - Usar Arduino IDE (1.0.5 ou superior recomendado)
   - Selecionar Board: Arduino Uno
   - Fazer upload do firmware

4. **Configurar via Serial**
   - Conectar via terminal serial em 115200 baud
   - Usar comandos `$` para configuração
   - Exemplo: `$$` para ver todas as configurações

5. **Testar Movimento**
   - Usar software como CNCjs, Lightburn ou LaserWeb
   - Enviar comandos G-code simples
   - Validar movimento dos eixos e laser

***
![GitHub Logo](https://github.com/gnea/gnea-Media/blob/master/Grbl%20Logo/Grbl%20Logo%20250px.png?raw=true)

## 📚 Referências e Recursos

- **GRBL Wiki**: https://github.com/grbl/grbl/wiki
- **Licença**: Grbl é software livre, lançado sob a licença GPLv3

### Créditos do GRBL:

- **Desenvolvedor Principal [2011 - Atual]**: Sungeun (Sonny) K. Jeon, Ph.D. (USA)
- **Originator/Criador [2009 - 2011]**: Simen Svale Skogsrud (Noruega)

***

## 📝 Changelog

Consulte a documentação na pasta `/doc/log/` para histórico completo de versões e mudanças.

***

_Grbl v1.1 e versões posteriores disponíveisl em [releases](https://github.com/gnea/grbl/releases)_
