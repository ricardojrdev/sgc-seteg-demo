# 📁 Estrutura do Projeto SGC Seteg

## Organização de Pastas

```
sgc-seteg/
├── public/                          # Arquivos públicos
│   ├── doc/                         # Documentos (vazio - imagens movidas)
│   ├── index.html                   # Página principal
│   └── test.html                    # Página de testes
│
├── src/                             # Código fonte
│   ├── assets/                      # Recursos estáticos
│   │   ├── icons/                   # Ícones do projeto (vazio)
│   │   └── images/                  # Imagens do projeto
│   │       ├── bg-azul.png          # Background modo dark
│   │       ├── bg-branco.png        # Background modo light
│   │       ├── logo-branco.png      # Logo para modo dark
│   │       ├── logo-preto.png       # Logo para modo light
│   │       └── favicon.png          # Ícone do site
│   │
│   ├── css/                         # Estilos
│   │   └── style.css                # CSS principal com temas
│   │
│   └── js/                          # JavaScript
│       ├── app.js                   # Aplicação principal
│       ├── firebase/                # Configuração Firebase
│       │   └── firebase-config.js
│       ├── modules/                 # Módulos da aplicação
│       │   ├── auth-module.js
│       │   ├── cartography-data-module.js
│       │   └── map-module.js
│       └── utils/                   # Utilitários
│           └── dom-utils.js
│
├── docs/                            # Documentação
│   └── MELHORIAS_UI.md              # Lista de melhorias visuais
│
├── .kiro/                           # Configurações Kiro (se existir)
│
├── iniciar-servidor.bat             # Script para iniciar servidor
├── iniciar-servidor-e-abrir.bat    # Script com abertura automática
├── parar-servidor.bat               # Script para parar servidor
├── LEIA-ME.txt                      # Instruções rápidas
├── COMO_EXECUTAR.md                 # Guia de execução
├── ESTRUTURA_PROJETO.md             # Este arquivo
└── README.md                        # Documentação principal

```

## 🎨 Convenções de Nomenclatura

### Imagens
- **Backgrounds**: `bg-[tema].png`
  - `bg-azul.png` - Fundo escuro
  - `bg-branco.png` - Fundo claro

- **Logos**: `logo-[cor].png`
  - `logo-branco.png` - Logo clara (para fundo escuro)
  - `logo-preto.png` - Logo escura (para fundo claro)

- **Ícones**: `favicon.png`

### Arquivos JavaScript
- **Módulos**: `[nome]-module.js`
- **Utilitários**: `[nome]-utils.js`
- **Configuração**: `[nome]-config.js`

### Arquivos CSS
- **Principal**: `style.css`
- **Temas**: Definidos via CSS variables e `[data-theme]`

## 📂 Localização de Recursos

### Imagens
Todas as imagens devem estar em: `src/assets/images/`

### Ícones
Todos os ícones devem estar em: `src/assets/icons/`
(Atualmente usando Bootstrap Icons via CDN)

### Estilos
Todos os arquivos CSS em: `src/css/`

### Scripts
Todos os arquivos JavaScript em: `src/js/`

## 🔗 Caminhos nos Arquivos

### No HTML
```html
<!-- Imagens -->
<img src="/src/assets/images/logo-branco.png" />

<!-- CSS -->
<link rel="stylesheet" href="/src/css/style.css" />

<!-- JavaScript -->
<script type="module" src="/src/js/app.js"></script>
```

### No CSS
```css
/* Imagens */
background-image: url("/src/assets/images/bg-azul.png");
content: url("/src/assets/images/logo-branco.png");
```

## 📝 Notas Importantes

1. **Caminhos Absolutos**: Use caminhos começando com `/` para garantir que funcionem de qualquer lugar
2. **Assets Organizados**: Mantenha imagens em `images/` e ícones em `icons/`
3. **Nomenclatura Clara**: Use nomes descritivos que indiquem o propósito do arquivo
4. **Temas**: Imagens específicas de tema devem ter o tema no nome (ex: `bg-azul`, `logo-branco`)

## 🚀 Servidor Local

O servidor roda na raiz do projeto, então todos os caminhos são relativos a `sgc-seteg/`

Acesso: `http://localhost:8080/public/index.html`
