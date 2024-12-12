
# 🌿 Smart-Garden Hardware 🔧

Este projeto integra sensores de solo e uma rede MQTT para monitoramento em tempo real de dados ambientais! 📡🌱

---

## 📦 Funcionalidades

- **📡 Leitura de Sensores via Modbus**:
  - Umidade do solo (%RH)
  - Temperatura do solo (°C)
  - Condutividade elétrica

- **📤 Envio de Dados via MQTT**:
  - Transmite os dados lidos para um broker MQTT.

---

## 🛠️ Tecnologias Utilizadas

- **Modbus**: Para comunicação com sensores.
- **Paho MQTT**: Cliente MQTT para envio de dados.
- **Python**: Linguagem de programação.

---

## 🚀 Como Rodar o Projeto

1. **Instale as dependências**:

   ```bash
   pip install paho-mqtt pymodbus
   ```

2. **Configure a porta Modbus e o broker MQTT** no `main.py`:

   ```python
   # Configuração do cliente Modbus
   port='COM3'  # Ajuste para sua porta serial

   # Configuração do cliente MQTT
   mqtt_client.connect("localhost", 1883, 60)  # Ajuste o endereço do broker
   ```

3. **Execute o script**:

   ```bash
   python main.py
   ```

---

## 📝 Estrutura do Projeto

```
smart-garden-hardware/
│-- main.py
```

---

## 📝 Explicação do Código

- **Leitura Modbus**: Os dados são lidos dos registradores do sensor.
- **Envio MQTT**: Os dados são publicados em um tópico MQTT para integração com outros sistemas.

---

🌱 **Happy Gardening!** 🌿
