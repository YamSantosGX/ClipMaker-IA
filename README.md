# ClipMaker IA 🎬

Uma aplicação web inovadora que utiliza inteligência artificial para extrair os momentos mais virais de seus vídeos automaticamente.

## 📋 Sobre o Projeto

**ClipMaker IA** é um projeto desenvolvido através do programa de aprendizado guiado da **Rocketseat**, focado em ensinar como integrar e utilizar inteligência artificial em aplicações web modernas. A aplicação combina tecnologias de upload de mídia, processamento de áudio e análise inteligente para identificar automaticamente os melhores momentos de um vídeo para criar clips viraliz áveis.

### Objetivo Principal

Transformar vídeos longos em clips de 30-60 segundos otimizados para redes sociais, utilizando a IA do Google Gemini para analisar transcrições e identificar momentos com maior potencial viral.

## 🎯 Funcionalidades Principais

- ✨ **Upload de Vídeos**: Interface intuitiva para fazer upload de vídeos via Cloudinary
- 🤖 **Análise com IA**: Utiliza o Google Gemini para analisar transcrições de áudio
- 🎬 **Extração de Clips**: Identifica e extrai automaticamente os melhores momentos (30-60 segundos)
- 📊 **Transcrição Automática**: Converte áudio em texto para análise de conteúdo
- 🎨 **Interface Moderna**: Design responsivo com animações suaves usando GSAP
- 🎪 **Validação de API**: Sistema de autenticação com chave de API Gemini
- ⚡ **Feedback em Tempo Real**: Feedback visual durante o processamento

## 📄 Páginas da Aplicação

### 1. **Página Principal (index.html)**
- Seção de entrada com campo para API Key do Gemini
- Botão principal "Começar Upload"
- Exibição de estado de carregamento com mensagens dinâmicas
- Visualizador de vídeo/clip gerado
- Animações de entrada e transições suaves

## 🔧 Funções Principais

### Objeto `app` - Gerenciamento de Aplicação

**`waitForTranscription()`**
- Aguarda a disponibilidade da transcrição do vídeo na Cloudinary
- Faz até 30 tentativas a cada 2 segundos
- Retorna `true` quando a transcrição está pronta

**`getTranscription()`**
- Recupera o arquivo de transcrição de texto da Cloudinary
- Retorna o conteúdo em formato texto

**`getViralMoment()`**
- Integra com a API do Google Gemini 2.5 Flash
- Envia a transcrição como prompt personalizado
- Recebe coordenadas de início e fim do melhor momento
- Retorna string formatada: `so_XX,eo_XX`

### Objeto `el` - Manipulação do DOM

Referências centralizadas para elementos da página:
- `loading`: Indicador de carregamento
- `video`: Elemento de vídeo
- `error`: Container de erro
- `apiKey`: Campo de entrada da API Key
- `uploadButton`: Botão de upload

### Widget Cloudinary

**`myWidget`**
- Gerencia o upload de vídeos
- Configura tema visual para a interface
- Executa workflow completo após upload bem-sucedido
- Trata erros com mensagens amigáveis

### Animações GSAP

**Timeline de Inicialização**
- Anima entrada do header
- Anima seção CTA (Call To Action)
- Anima área de vídeo
- Usa easing exponencial para transições suaves

## 💻 Tecnologias Utilizadas

### Frontend
- **HTML5** - Estrutura semântica da aplicação
- **CSS3** - Estilização com classes personalizadas
- **Tailwind CSS** - Framework de utilitários para design responsivo
- **JavaScript (Vanilla)** - Lógica pura sem dependências pesadas

### Bibliotecas e APIs
- **GSAP (GreenSock Animation Platform)** - Animações fluidas e timeline
- **Lucide Icons** - Sistema de ícones SVG modern
- **Cloudinary** - Upload, armazenamento e processamento de mídia
- **Google Gemini API** - Inteligência artificial para análise de conteúdo

### Serviços Externos
- **Google Cloud Generative AI (Gemini 2.5 Flash)** - Modelo de IA para análise de transcrições
- **Cloudinary** - Hospedagem de vídeos e geração de transcrições automáticas

### Design e UX
- **Inter Font** (Google Fonts) - Tipografia principal
- **Backdrop Filters** - Efeitos glass-morphism
- **Gradientes e Blur** - Efeitos visuais modernos

## 🚀 Como Usar

1. **Obtenha uma API Key do Gemini**
   - Acesse [Google AI Studio](https://aistudio.google.com)
   - Crie uma nova chave de API

2. **Acesse a Aplicação**
   - Abra o `index.html` em seu navegador

3. **Insira sua API Key**
   - Cole sua chave Gemini no campo indicado

4. **Faça Upload de um Vídeo**
   - Clique em "Começar Upload"
   - Selecione um vídeo do seu dispositivo

5. **Aguarde o Processamento**
   - A aplicação aguardará a transcrição
   - A IA analisará para encontrar o melhor momento
   - O clip será exibido automaticamente

## 📚 Conceitos Aprendidos (Conforme Rocketseat)

Este projeto ensina:

- ✅ Integração com APIs externas (Cloudinary, Google Gemini)
- ✅ Manipulação de elementos DOM com JavaScript puro
- ✅ Promises e tratamento assíncrono
- ✅ Design com Tailwind CSS
- ✅ Animações avançadas com GSAP
- ✅ Integração de modelos de IA em aplicações web
- ✅ Tratamento de erros e feedback ao usuário
- ✅ Utilização de APIs RESTful
- ✅ Deploy com GitHub Pages

## 🎨 Design Highlights

- **Tema Escuro Moderno**: Paleta de cores azul e índigo sobre fundo escuro
- **Glass Morphism**: Efeitos de vidro com backdrop filters
- **Animações Suaves**: Transições com curva de easing exponencial
- **Responsive**: Funciona perfeitamente em dispositivos móveis e desktop
- **Acessibilidade**: Ícones e textos claros e bem contrastados

## 📦 Estrutura do Projeto
ClipMaker-IA/ ├── index.html # Página principal da aplicação ├── draw.excalidraw # Diagramas de design/arquitetura └── README.md # Este arquivo

## 🔐 Variáveis de Configuração

No objeto `app`, encontram-se as seguintes configurações:

- `cloudName`: Nome da conta Cloudinary
- `uploadPreset`: Preset de upload pré-configurado
- `model`: Modelo Gemini utilizado (gemini-2.5-flash)

## ⚠️ Requisitos

- Navegador moderno com suporte a Fetch API
- Chave de API válida do Google Gemini
- Vídeo em formato compatível (MP4, WebM, etc)
- Conexão com internet

## 🎓 Este Projeto é Resultado de

Aprendizado estruturado através da **Rocketseat**, plataforma focada em ensinar desenvolvimento web com as melhores práticas da indústria e tecnologias em alta demanda.

---

**Feito com 💜 e código por mim e graças a Rocketseat**
