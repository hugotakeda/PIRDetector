---

# PIRDetector

Sistema de detecção de movimento utilizando um sensor PIR e um Raspberry Pi, com notificações enviadas via Telegram.

## Descrição

Este projeto utiliza um sensor infravermelho passivo (PIR) conectado a um Raspberry Pi para detectar movimentos. Quando um movimento é detectado, o sistema captura uma imagem através da câmera do Raspberry Pi e a envia para um chat ou grupo do Telegram pré-configurado.

## Funcionalidades

* Detecção de movimento em tempo real.
* Captura de fotos automática ao detectar presença.
* Notificações instantâneas via bot do Telegram.
* Logs de atividade para monitoramento.

## Pré-requisitos

Antes de começar, você precisará de:

* Raspberry Pi (qualquer modelo com GPIO e suporte a câmera).
* Módulo de Câmera do Raspberry Pi.
* Sensor de movimento PIR (HC-SR501).
* Jumpers (cabos conectores).
* Python 3 instalado.

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/hugotakeda/PIRDetector.git
   cd PIRDetector
   ```

2. Instale as dependências necessárias:
   ```bash
   pip install -r requirements.txt
   ```

3. Configure suas credenciais do Telegram no arquivo de configuração (ou variáveis de ambiente, conforme estruturado no código).

## Configuração do Hardware

* **VCC do PIR** -> 5V no Raspberry Pi
* **GND do PIR** -> GND no Raspberry Pi
* **OUT do PIR** -> GPIO 7 (ou o pino definido no código)

## Como usar

Execute o script principal para iniciar o monitoramento:

```bash
python main.py
```

---
