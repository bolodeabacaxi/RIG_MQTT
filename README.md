# 🌐 Monitoramento de Rig com ESP32 e MQTT

Este projeto utiliza o **ESP32** para monitorar sua rig de mineração e enviar atualizações para um servidor **MQTT**. Ideal para quem quer monitorar sua rig remotamente via MQTT, podendo integrar com outras ferramentas ou dashboards.

---

## 🚀 Funcionalidades

- 🌐 **Conexão automática ao Wi-Fi**.
- 📡 **Integração com MQTT** para comunicação em tempo real.
- ⚡ **Envio de mensagens periódicas**, informando o status da rig.

---

## 📦 Requisitos

- **ESP32** (Placa de desenvolvimento)
- **Arduino IDE** ou **PlatformIO**
- **Broker MQTT** (Pode usar o [Mosquitto](https://mosquitto.org/) ou qualquer outro servidor MQTT)
- Bibliotecas: `WiFi.h`, `PubSubClient.h`

---

## 🛠️ Como Usar

1. **Configuração do Wi-Fi**:
   - Substitua os valores de `ssid` e `password` com as credenciais da sua rede Wi-Fi.

2. **Configuração do MQTT**:
   - Substitua `mqttServer` com o endereço IP ou hostname do seu broker MQTT.
   - Deixe `mqttPort` como 1883, ou altere se o seu broker usar outra porta.
   - Substitua `mqttTopic` com o tópico desejado para publicar as mensagens.

3. **Carregue o Código no ESP32**:
   - Abra o código no **Arduino IDE** ou **PlatformIO**.
   - Carregue no seu **ESP32**.

4. **Monitoramento**:
   - O ESP32 vai se conectar ao seu Wi-Fi e broker MQTT, e começar a enviar mensagens periódicas, como o status "⚡ Rig funcionando!".

---

## 📨 Como Funciona

1. **Conexão Wi-Fi**: O ESP32 conecta-se automaticamente à sua rede Wi-Fi usando as credenciais fornecidas.
2. **Conexão MQTT**: O ESP32 se conecta ao servidor MQTT para começar a enviar mensagens.
3. **Mensagens Periódicas**: A cada 1 minuto, o ESP32 publica no tópico MQTT configurado, enviando a mensagem "⚡ Rig funcionando!".

---

## 📱 Testando a Integração

Você pode testar a integração com o **MQTT Explorer** ou **Node-RED** para ver as mensagens chegando no seu broker MQTT em tempo real.

### Testando com MQTT Explorer:
1. Abra o MQTT Explorer.
2. Conecte-se ao seu broker MQTT utilizando as mesmas configurações de IP e porta.
3. Inscreva-se no tópico configurado (por exemplo, `mining/rig`).
4. Veja as mensagens sendo publicadas pelo ESP32!
