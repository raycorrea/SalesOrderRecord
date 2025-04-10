# 🌐 Projeto Arduino com Ethernet, Sensor de Temperatura e Controle de LEDs RGB

Esse é um projeto feito com Arduino que conecta o microcontrolador a uma rede usando Ethernet e permite controlar LEDs RGB e um LED comum através de uma página web. Também usamos um sensor de temperatura (termistor) e um sensor de luminosidade (LDR) para mostrar algumas informações legais na mesma página.

## 🤔 O que esse projeto faz?

Quando você liga o Arduino e conecta ele à rede:

- Um servidor web é iniciado.
- Através do navegador (digitando o IP do Arduino), você pode acessar uma página simples.
- Nessa página, você consegue:
  - Ligar e desligar um LED.
  - Controlar as cores de um LED RGB (vermelho, verde e azul combinados).
  - Ver a temperatura atual medida por um termistor.
  - Ver se está de dia ou de noite com base na leitura de luz ambiente (usando um sensor LDR).

---

## 🧠 Componentes usados

- Arduino Uno
- Módulo Ethernet (W5100)
- LED comum
- LED RGB
- Sensor de temperatura (termistor)
- Sensor de luminosidade (LDR)
- Cabos, resistores, etc.

---

## ⚙️ Como funciona o código

### Conexão com a internet
O Arduino se conecta à sua rede local com IP fixo:

```cpp
byte ip[] = { 192, 168, 0, 32 };
```

### Página HTML simples
O Arduino cria uma página acessível no navegador, com botões para:

- `/?ledon` → Liga o LED
- `/?ledoff` → Desliga o LED
- `/?cor1` até `/?cor7` → Mudam as cores do LED RGB
- Mostra temperatura e luminosidade

### Sensores
- O termistor mede a **temperatura** e mostra na tela.
- O sensor de luz lê a **luminosidade** e diz se está "Dia" ou "Noite".

---

## 😅 Desafios que enfrentei

- Entender como funciona a comunicação HTTP no Arduino usando Ethernet.
- Organizar as condições com os comandos recebidos do navegador.
- Aprender a usar `analogRead()` e `digitalWrite()` em conjunto com as condições.
- Exibir corretamente as informações na página HTML enviada pelo Arduino.

---

## 📸 Print da página (se quiser adicionar uma imagem futuramente)

> *Aqui você pode colocar uma imagem de como a página aparece no navegador.*

---

## 🚀 O que posso melhorar?

- Criar um controle mais bonito com sliders para ajustar as cores com mais precisão.
- Mostrar os dados de temperatura e luminosidade com gráficos (em JavaScript, por exemplo).
- Melhorar o HTML da página para ficar mais moderno.

---

## 🛠️ Requisitos para rodar

- Placa Arduino Uno
- Módulo Ethernet W5100
- IDE do Arduino instalada
- Biblioteca `Thermistor` instalada na IDE
