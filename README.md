Com certeza! Adicionei uma nova seção de **Contribuintes** com links diretos para os perfis do GitHub, mantendo o estilo visual do seu documento.

Aqui está o conteúdo atualizado para o seu `README.md`:

---

# 🛰️ Sistema de Monitoramento Inteligente com TTGO T-Camera + Notificações em Tempo Real

Sistema IoT desenvolvido com **TTGO T-Camera ESP32**, sensor PIR, OLED display e envio de alertas via **Discord** com captura de imagem em tempo real. Também fornece um **dashboard web** com histórico de eventos e suporte a transmissão ao vivo (MJPEG).

> 💡 Projeto baseado e expandido a partir de: [RobotZero.one - TTGO Security Camera with PIR Motion Sensor](https://robotzero.one/ttgo-security-camera-pir/)

---

## 🧠 Principais Funcionalidades

* ✅ Detecção de movimento com sensor PIR (HC-SR501)
* 📸 Captura de imagem automática via câmera integrada
* ⏰ Registro de data/hora via NTP
* 💬 Envio de notificação com imagem para Discord (`@everyone`)
* 🖥️ Interface web para visualização de logs
* 🌐 Comunicação em tempo real via WebSocket
* 📺 Transmissão MJPEG (live stream via navegador)
* 🧾 Armazenamento local de eventos (JSON)
* 🧩 Display OLED 0.96” com feedback visual

---

## 👥 Contribuintes

Este projeto foi desenvolvido e é mantido por:

* **Éden Samuel** - [GitHub](https://github.com/Eden-code01)
* **Fernando Lopes** - [GitHub](https://github.com/Fernando-Lopes1)

---

## 🔧 Componentes Utilizados

| Componente | Modelo / Especificação |
| --- | --- |
| Placa ESP32 | TTGO T-Camera ESP32 WROVER + lente olho de peixe |
| Câmera | OV2640 integrada |
| Sensor de movimento | PIR (HC-SR501) |
| Display OLED | SSD1306 128x64 I2C |
| Conectividade | Wi-Fi 2.4GHz |

---

## 📁 Estrutura de Diretórios

```text
.
├── arduino/
│   ├── main.ino
│   └── config.h
├── server/
│   ├── server.py
│   ├── index.html
│   └── logs.json
├── LICENSE
└── README.md

```

---

## ⚙️ Como Configurar

### 1. ⚡ Conexões do Hardware (TTGO T-Camera)

| Pino ESP32 | Componente |
| --- | --- |
| GPIO33 | Saída do Sensor PIR |
| I2C (21/22) | Display OLED |

---

### 2. 📲 Código Arduino

**Arquivo:** `arduino/main.ino`

```cpp
const char* ssid = "SUA_REDE_WIFI";
const char* password = "SUA_SENHA_WIFI";
const char* discordWebhook = "URL_DO_SEU_WEBHOOK_DISCORD";

```

> 💡 Compile com:
> * Placa: **ESP32 Wrover Module**
> * Frequência: 240 MHz
> * PSRAM: Habilitada
> 
> 

---

### 3. 💻 Backend com Node.js

#### Instalação

```bash
cd server
npm install

```

#### Executar o servidor

```bash
node server.js

```

#### Endpoints disponíveis

* `GET /` — Dashboard Web
* `GET /logs` — Lista de eventos (JSON)
* `POST /log` — Adicionar evento (usado pelo ESP32)

---

## 🌐 Acesso ao Sistema

* **Dashboard Web:** [`http://localhost:3000`](https://www.google.com/search?q=http://localhost:3000)
* **Live Stream (ESP32):** [`http://<IP-DO-ESP32>`](https://www.google.com/search?q=http://%3CIP-DO-ESP32%3E)
* **Notificações:** via Discord Webhook com imagem

---

## 📦 Bibliotecas Recomendadas (Arduino IDE)

* `ESPAsyncWebServer`
* `ESPAsyncTCP`
* `esp_camera`
* `WiFi`
* `HTTPClient`
* `ArduinoJson`
* `Adafruit_SSD1306`
* `Adafruit_GFX`
* `NTPClient`

---

## 📸 Exemplo de Notificação no Discord

```
📷 Movimento Detectado!
🕒 Horário: 19/06/2025 às 15:42:10
🔗 [Imagem Capturada](URL_DA_IMAGEM)

```

---

## 🧪 Futuras Melhorias (To-Do)

* [ ] Integração com Telegram
* [ ] Reconhecimento facial básico
* [ ] Armazenamento em nuvem (Firebase ou Google Drive)
* [ ] Autenticação de usuários no dashboard

---

## 🤝 Créditos

* [RobotZero.one](https://robotzero.one/ttgo-security-camera-pir/)
* [LilyGO TTGO](https://www.lilygo.cc/)
* Comunidade ESP32 no GitHub e fóruns

---

## 📄 Licença

Este projeto está licenciado sob os termos da [Licença MIT](https://www.google.com/search?q=LICENSE).

---

💬 **Contribuições são bem-vindas!** Abra uma *issue* ou envie um *pull request* com melhorias.

---

Seria interessante eu gerar uma imagem ilustrativa de como ficaria o dashboard do sistema para você colocar no README?
