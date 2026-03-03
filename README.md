# SGC Seteg - Sistema de Gestão Cartográfica

Este repositório contém a base do **SGC Seteg**, um sistema web simples porém estruturado para crescer, usando apenas **HTML, CSS e JavaScript puro**, com **Firebase Realtime Database**.

## Arquitetura de pastas

```text
sgc-seteg/
├── public/
│   ├── index.html
│   └── doc/            # Imagens e artefatos estáticos visíveis pelo navegador
│
├── src/
│   ├── assets/
│   │   ├── images/
│   │   └── icons/
│   │
│   ├── css/
│   │   └── style.css
│   │
│   ├── js/
│   │   ├── app.js
│   │   ├── firebase/
│   │   │   └── firebase-config.js
│   │   ├── modules/
│   │   │   ├── map-module.js
│   │   │   ├── auth-module.js
│   │   │   └── cartography-data-module.js
│   │   └── utils/
│   │       └── dom-utils.js
│   │
│   └── components/
│
├── docs/
├── .gitignore
└── README.md
```

## Como executar

1. Abra `public/index.html` no navegador (duplo clique ou via servidor estático simples).
2. Certifique‑se de que a pasta `public/doc` contenha os arquivos de imagem utilizados no CSS e no HTML (por exemplo `LOGO.png`, `plano_fundo.png`).
3. O Firebase é carregado via CDN a partir de `src/js/firebase/firebase-config.js`.  
   - O arquivo já está isolado em um módulo próprio e expõe apenas o necessário via `window`.

## Pontos de extensão

- `src/js/modules/map-module.js`: ponto de entrada para integrar Leaflet ou OpenLayers.
- `src/js/modules/auth-module.js`: futuro módulo de autenticação (ex.: Firebase Auth).
- `src/js/modules/cartography-data-module.js`: centralização de dados cartográficos (WMS/WFS/GeoJSON).

Toda a lógica atual de **solicitações cartográficas** está em `src/js/app.js`, organizada em blocos (init, Firebase, formulário, tabela, relatórios, helpers), com uma função `init()` que é o ponto único de inicialização da aplicação.

