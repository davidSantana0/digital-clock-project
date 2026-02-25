# 📝 Documentação Técnica: Relógio Digital

Este diretório contém a implementação de um relógio digital dinâmico. O foco deste exercício foi a integração entre lógica de tempo em JavaScript e estilização avançada em CSS.

## 🗂️ Arquivos do Projeto

* **`index.html`**: Estrutura semântica contendo os containers de exibição (`hours`, `minutes`, `seconds`).
* **`digital-clock.css`**: Estilização visual com uso de Flexbox, Gradientes e Glassmorphism.
* **`digital-clock.js`**: Lógica de captura de tempo e manipulação do DOM.

---

## ⚙️ Funcionamento do Código

### 1. Captura de Tempo

O script utiliza o objeto `new Date()` para extrair as informações do sistema do usuário:

```javascript
let now = new Date();
let realTimeHours = now.getHours().toString().padStart(2, '0');

```

### 2. O Método `padStart(2, '0')`

Uma implementação crucial para a interface. Ela garante que, se o valor for menor que 10 (ex: 5 segundos), o JavaScript adicione um "0" à esquerda, mantendo o relógio sempre com o formato `00:00:00`.

### 3. Atualização Contínua

Foi utilizado o `setInterval` com um intervalo de **1000ms**, garantindo que o relógio atualize o valor dos segundos em tempo real sem a necessidade de recarregar o navegador.

---

## 🎨 Design e UI

* **Paleta de Cores**: Gradiente entre `#7B1FA2` (Purple) e `#9C27B0` (Fuchsia).
* **Layout**: O uso de `display: flex` no container garante que os elementos fiquem alinhados e centralizados em qualquer resolução de tela.
* **Interatividade**: As caixas possuem sombras internas e externas para criar profundidade.

---

## 📌 Notas de Desenvolvimento

Este projeto foi desenvolvido aplicando os princípios de:

* **Clean Code**: Nomes de variáveis semânticos.
* **DRY (Don't Repeat Yourself)**: Lógica centralizada dentro de um único intervalo.
* **Performance**: Atualização pontual apenas dos elementos necessários no DOM.

---

**David Santana** | *Estudo de Fundamentos Web*

---