# Projetos de Sistemas Embarcados - EmbarcaTech 2025

Autor: **Igor Kenzo M. Sebata**

Curso: Residência Tecnológica em Sistemas Embarcados

Instituição: EmbarcaTech - HBr

Campinas, maio de 2025

---

## 📌 Proposta
Este projeto visa implementar um "Digital Twin" de uma Placa de Galton em um display OLED utilizando a BitDogLab.

---

## 🎯 Objetivo
- Criar uma representação visual e interativa da distribuição normal
- Simular bolinhas caindo através de uma matriz triangular de pinos, onde cada pino representa uma decisão binária aleatória (esquerda ou direita).
- Demonstrar visualmente o histograma gerado pelo acumulo de bolinhas em cada "cesta" (bin)

---

## 🧩 Componentes Usados
- Raspberry Pi Pico
- OLED I2C SSD1306
- Joystick

---

## ⚡ Pinagem dos Dispositivos
| Componente | Pino do Pico |
|------------|--------------|
| **OLED SSD1306 (SDA)** | 14 |
| **OLED SSD1306 (SCL)** | 15 |
| **Joystick Y** | 26 |
| **Joystick X** | 27 |
| **Joystick SW** | 22 |

---

## 📈 Resultados Esperados

- Distribuição que se aproxima de uma curva normal no histograma.
- Maior concentração de bolinhas na região central.
- Diminuição da frequência perto das extremidades do histograma.

## Reflexão Final
### 1. O foi observado sobre o padrão dos resultados?
As bolinhas tendem a se concentrar no centro do histograma, formando uma distribuição que se aproxima de uma curva normal.

### 2. A simulação confirma a teoria da distribuição normal?
Sim, a simulação confirma visualmente os princípios da distribuição normal. A decisão binária da bolinha ao colidir com os pinos, ao longo do caminho, embora aleatória, faz com que estas tendam ao centro.

### 3. Qual tipo de desbalanceamento você sugere em uma inclusão futura nesta simulação?
Pinos específicos com "campos magnéticos" que atraem ou repelem as bolinhas.

### 4. Você teve alguma ideia para tornar a simulação mais interativa ou visual?
A adição de um acelerômetro para forçar o favorecimento para um dos lados, e cores RGB no display OLED.

---

## 🧪 Como Compilar e Executar
### Pré-Requisitos:
- BitDogLab
- Pico SDK
- CMake

### Passos:
1. Abra o projeto no VS Code, usando o ambiente com suporte ao SDK do Raspberry Pi Pico (CMake + compilador ARM);
2. Compile o projeto normalmente (Ctrl+Shift+B no VS Code ou via terminal com cmake e make);
3. Conecte a BitDogLab via cabo USB e coloque a Pico no modo de boot (pressione o botão BOOTSEL e conecte o cabo);
4. Copie o arquivo .uf2 gerado para a unidade de armazenamento que aparece (RPI-RP2);

---

## 📄 Licença
Este projeto está licenciado sob a [GNU General Public License v3.0](/LICENSE)

---

### 🔗 Referências
- [Documentação do Raspberry Pi Pico](https://www.raspberrypi.com/documentation/pico-sdk/)
- [Biblioteca SSD1306](https://github.com/daschr/pico-ssd1306)
