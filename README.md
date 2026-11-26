[readme_conversor_ergon_mico_100_madeira.md](https://github.com/user-attachments/files/35443845/readme_conversor_ergon_mico_100_madeira.md)
# Conversor Ergonômico 100% Madeira — Manual Técnico Interativo 3D

[![Acessar Manual 3D](https://img.shields.io/badge/Acessar_Manual_3D-Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://heroic-gumdrop-ed4b7b.netlify.app/)
[![Three.js](https://img.shields.io/badge/Three.js-0.160-black?style=for-the-badge&logo=three.js&logoColor=white)](https://threejs.org/)
[![Desktop Only](https://img.shields.io/badge/Compatibilidade-Apenas_Desktop-E86A42?style=for-the-badge)](#aviso-de-compatibilidade)

Manual técnico interativo em **3D** para construção de um conversor de mesa ergonômico (*standing desk converter*) feito **100% em compensado naval 18 mm**, utilizando a **Solução 1: Cremalheira Horizontal na Base + Escora Articulada em "U"**.

### Acesse o projeto online
**[Abrir Manual Técnico Interativo 3D no Netlify](https://heroic-gumdrop-ed4b7b.netlify.app/)**

---

## Aviso de Compatibilidade

> **Atenção:** Esta aplicação foi projetada e otimizada **exclusivamente para Desktop (versão computador)**. Para aproveitar corretamente o palco 3D interativo, os controles de câmera, a vista explodida e o painel técnico lateral, acesse utilizando um computador ou notebook.

---

## Sobre o Projeto

O objetivo deste projeto é oferecer uma alternativa **100% manual, barata e mecanicamente segura** para trabalhar sentado e em pé sobre uma mesa fixa comum, sem depender de motores, pistões ou serralheria.

### Destaques de Engenharia
* **Zero colisão com a mesa fixa:** os 3 dentes de travamento ficam esculpidos nas duas cremalheiras horizontais apoiadas na base, mantendo **1,0 cm de madeira maciça** abaixo do bastão Ø20 mm em todos os níveis.
* **4 posições ergonômicas** (referência sobre mesa fixa de 73 cm):
  * **Fechado (`4,37°`):** `81,2 cm` (`+8,2 cm`)
  * **N1 — Médio (`35°`):** `102,1 cm` (`+29,1 cm`)
  * **N2 — Alto (`47°`):** `108,7 cm` (`+35,7 cm`)
  * **N3 — Em Pé (`59°`):** `114,0 cm` (`+41,0 cm`) — calibrado para estatura de 1,80 m
* **Planos X independentes com folga real de 2 mm:** arruelas lisas M8 separam todas as articulações de madeira para evitar atrito e garantir dobramento plano.
* **Custo estimado:** ~R$ 168,00 (compensado naval 18 mm, parafusos M8, arruelas, porcas parlock e bastão Ø20 mm).

### Recursos do Manual Interativo
* **Palco 3D com Three.js:** câmeras dedicadas (`Iso`, `Lateral`, `Articulação`, `Trava`), modo **Tampo Raio-X** e controle de **Vista Explodida**.
* **Simulação de destravamento:** animação completa do gesto de alívio (+2°), levantamento da escora e descida suave até fechar.
* **4 abas técnicas:**
  * `01 Montagem` — passo a passo ilustrado + legenda interativa das camadas X.
  * `02 Cortes` — lista com 17 peças em compensado 18 mm com destaque em tempo real no 3D.
  * `03 Custos` — checklist interativa de materiais e ferragens.
  * `04 Ergo` — calculadora de altura conforme a mesa fixa e a estatura do usuário.

---

## Como baixar e rodar localmente (para aperfeiçoar o projeto)

Como toda a aplicação roda em um **único arquivo HTML** utilizando ES Modules via CDN (sem necessidade de `npm install` ou etapa de build), é muito simples baixar e modificar o código.

### Pré-requisitos
* [Git](https://git-scm.com/) instalado (opcional, você também pode baixar o `.zip` direto pelo GitHub).
* Um navegador moderno no computador (Chrome, Edge, Firefox ou Brave).
* Um servidor local simples (ex.: extensão **Live Server** no VS Code, Python ou Node.js) para evitar bloqueios de CORS ao carregar os módulos do Three.js.

### Passo a passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/gabrielisbo/conversor-ergonomico-madeira.git
   ```

2. **Acesse a pasta do projeto:**
   ```bash
   cd conversor-ergonomico-madeira
   ```

3. **Inicie um servidor local (escolha a opção que preferir):**

   * **Com VS Code (recomendado):**
     1. Abra a pasta no VS Code.
     2. Instale a extensão **Live Server**.
     3. Clique com o botão direito em `index.html` e selecione **Open with Live Server**.

   * **Com Python 3:**
     ```bash
     python -m http.server 5500
     ```
     Depois acesse `http://localhost:5500` no navegador.

   * **Com Node.js:**
     ```bash
     npx serve .
     ```

4. **Edite e personalize:**
   * Toda a geometria paramétrica (medidas em centímetros, ângulos dos dentes e planos X) está centralizada no objeto `GEO` dentro do arquivo `index.html`.
   * Ao alterar medidas ou melhorias na interface, basta salvar o arquivo e recarregar o navegador.

---

## Tecnologias Utilizadas

* **HTML5 / CSS3** + **Tailwind CSS** (via CDN)
* **JavaScript (ES Modules)**
* **Three.js** (`OrbitControls` + modelagem paramétrica em escala 1:1 cm)
* **Netlify** (hospedagem estática)
