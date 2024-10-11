# 🍇Agnello Vinheria - Monitoramento Remoto de Vinhos🍷

Bem-vindo ao repositório de **Agnello Vinheria**! Este projeto realiza o monitoramento remoto das condições do ambiente em que os vinhos são armazenados, com foco em temperatura, umidade e luminosidade. Usamos um sistema baseado em **ESP32** com sensores **DHT22** e integração via **MQTT** para monitorar e exibir esses dados em um dashboard interativo. 🚀

## 🔧 Funcionalidades

- Monitoramento de temperatura, umidade e luminosidade dos vinhos em tempo real.
- Envio dos dados para um broker MQTT e visualização em um dashboard interativo.
- Integração com sensores DHT22 e sistema de alertas via MQTT para monitoramento contínuo.

## 📝 Instruções para Uso

### 1️⃣ Código ESP32 (Monitoramento via MQTT)

Este código realiza a leitura de dados dos sensores conectados ao ESP32 e envia as informações para o broker MQTT.

#### Componentes Utilizados:
- **ESP32** para comunicação Wi-Fi.
- **DHT22** para monitoramento de temperatura e umidade.
- **Sensor de luminosidade** via leitura analógica.

#### Principais Funções:
- Conexão com o Wi-Fi e broker MQTT.
- Publicação periódica dos dados dos sensores de temperatura, umidade e luminosidade.
- Função de callback para receber comandos via MQTT.

📡 **Wi-Fi e MQTT:** O ESP32 conecta-se à rede Wi-Fi configurada e publica os dados em tópicos MQTT. Caso haja desconexão, o sistema tenta reconectar automaticamente.

### 2️⃣ Dashboard (Monitoramento via Dashboard)

Esse código cria um dashboard interativo utilizando o **Dash** para exibir os dados coletados dos sensores.

#### Principais Funcionalidades:
- Recebe os dados de luminosidade, umidade e temperatura através de uma API FIWARE.
- Exibe gráficos atualizados a cada 10 segundos com os valores coletados dos sensores.
- Converte automaticamente os timestamps para o fuso horário do Brasil.

## ⚙️ Como Executar

### ESP32:
1. Carregue o código para o ESP32 usando o Arduino IDE ou o Wokwi.
2. Certifique-se de que o ESP32 está conectado à internet.

### Dashboard:
1. Execute o dashboard com o comando `python app.py`.
2. Acesse o dashboard em [http://localhost:8050](http://localhost:8050) para visualizar os dados em tempo real.

## 🌟 Tecnologias Utilizadas
- **ESP32** para monitoramento remoto.
- **MQTT** para comunicação eficiente entre dispositivos.
- **Dash & Plotly** para visualização gráfica dos dados.

## 📊 Visualização do Dashboard

Aqui está uma visualização do dashboard com gráficos de temperatura, umidade e luminosidade em tempo real:

![Dashboard Interativo](caminho/para/sua/imagem-dashboard.png)

## 📢 Contribuições

Sinta-se à vontade para abrir issues, fazer pull requests ou sugerir melhorias! Toda ajuda é bem-vinda! 😊

## 👥 Equipe

- **Gabriel Matias**: Coordenador do projeto, garantindo a aderência aos prazos e ao orçamento.
- **Nathan Craveiro**: Desenvolvedor de design e interface do usuário, responsável pela experiência do usuário e integração com o backend.
- **Vitor Eskes**: Desenvolvedor da lógica do servidor, gerenciamento da infraestrutura, automação de deploy e testes.
