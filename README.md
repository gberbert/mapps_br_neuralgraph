# NTT DATA | AXET-NeuralGraph 3D — Plataforma Cognitiva Desktop

> **Apresentação Executiva & Técnica do Produto Desktop Nativo de Inteligência Artificial**  
> *RAG Local-First Estrito • Grafo Neural Tridimensional em WebGL (Three.js) • Neuroplasticidade Sintética em Tempo Real • Zero Vazamento de Dados (Air-Gapped Ready)*

---

## 🌟 Visão Geral do Produto

O **AXET-NeuralGraph 3D** é um ecossistema corporativo desenvolvido pela **NTT DATA** para transformar acervos complexos de documentação técnica, regras de negócio de missão crítica (como **Reef.core**) e matrizes regulatórias em um universo tridimensional navegável de alta fidelidade:

1. **🌌 Grafo Neural 3D Anatômico (`brain.glb` + Three.js)**:
   - Mais de **3.111 nós documentais** e **9.472 sinapses** organizados espacialmente segundo a neuroanatomia real do cérebro humano (Lobos Temporal, Frontal, Parietal, Occipital, Cerebelo e Tronco Encefálico).
   - O Lobo Temporal armazena a memória declarativa & semântica (apólices ativas, contratos, 36% do grafo); o Lobo Parietal gerencia integrações técnicas e APIs; o Frontal orquestra decisões de negócio e governança.
2. **🧠 Neuroplasticidade Sintética & Auto-Retificação**:
   - O assistente identifica falhas no próprio raciocínio em tempo real durante a conversa, auto-retifica-se e muta a estrutura do Grafo e da Memória Vetorial imediatamente (gerando um nó `APRENDIZADO_COGNITIVO` com aresta `RETIFICA_CONCEITO` de peso 2.5+).
   - Perguntas futuras priorizam automaticamente essa diretriz canônica consolidada sobre documentações legadas.
3. **🌐 Federação via GitHub com Zero Permissões (Cenário 1)**:
   - Coleta contínua de sinapses de centenas de colaboradores via Outbox local e GitHub Issues com label `cognitive-learning`, **sem exigir credenciais ou acesso de gravação no repositório**.
   - Curadoria centralizada pelo Master Admin no painel web e compilação do pacote global (`.pack`), distribuído via GitHub Releases em menos de 2 segundos.
4. **🛡️ RAG Local-First Estrito & Blindagem Epistêmica**:
   - Isolamento total no localhost (`127.0.0.1`). Perguntas, chats e regras nunca saem da estação de trabalho.
   - Entrega de conhecimento por snapshots vetoriais compactados (`.qpack`), sem distribuição de texto puro em disco e com integridade verificada por SHA-256.
   - **Blindagem Epistêmica**: Anexos de chat (PDFs, PPTs, imagens) são efêmeros e rigorosamente proibidos de contaminar a memória permanente ou gerar novas sinapses (*imunidade contra data poisoning*).
5. **📎 Suporte Multimodal no Chat com Telemetria Dinâmica (SSE)**:
   - Leitura nativa em memória de PDFs corporativos, PowerPoint (com anotações de slide) e Word.
   - Visão computacional com redimensionamento inteligente Pillow (máx 1080p, até 3 imagens).
   - Indicador de status dinâmico via Server-Sent Events substituindo os tradicionais "3 pontinhos".
6. **⚖️ Matriz Regulatória & Glossário De ➔ Para**:
   - Módulo administrativo de gestão de órgãos reguladores por jurisdição (ex: SUSEP no Brasil, DGSFP na Espanha), com thesaurus semântico de termos de seguros e tecnologia.

---

## 🏗️ Arquitetura Tecnológica

| Camada | Tecnologias Principais | Destaques |
| :--- | :--- | :--- |
| **Desktop Shell** | **Tauri v2 (Rust)** | Binário nativo compilado, instaladores para macOS (`.dmg`) e Windows (`.msi`), consumo de RAM inferior a 100MB, seletor nativo de diretórios OneDrive. |
| **Frontend Reativo** | **Next.js 14 + Three.js** | App Router, WebGL a 60 FPS com `GLTFLoader`, Tailwind CSS, identidade visual NTT DATA e Lucide Icons. |
| **Backend API** | **FastAPI + Python 3.11** | Endpoints assíncronos, SSE para streaming de respostas cognitivas, Pydantic v2 e SQLAlchemy Asyncpg. |
| **Motores de IA** | **Qdrant + Postgres 16** | Busca vetorial HNSW aproximada por cosseno, persistência relacional de nós/sinapses e transcrição de áudio/vídeo via Faster-Whisper e FFmpeg. |

---

## 🖼️ Galeria de Telas Disponíveis

As imagens reais da aplicação estão organizadas no diretório `assets/`:
- `screen_neural_graph_3d.jpg`: Visualização 3D do encéfalo com 3.111 nós e 9.472 sinapses.
- `screen_node_inspection.jpg`: Inspeção detalhada de nó semântico com autoridade do Reef Academy.
- `screen_graph_immersive.jpg`: Assistente cognitivo imersivo recapitulando conversas anteriores.
- `screen_chat_streaming.jpg`: Chat com streaming SSE e status de processamento em tempo real.
- `screen_home_dashboard.jpg`: Dashboard inicial com perfil corporativo Okta SSO e perguntas sugeridas.
- `screen_admin_regulatory.jpg`: Painel administrativo com controle de jurisdições e regras De ➔ Para.
- `screen_sidebar_connections.jpg`: Gestão de sessões ativas e status de conexão RAG Local.

---

## 🚀 Como Executar Localmente

Abra o arquivo `index.html` em qualquer navegador moderno:
```bash
open "/Users/gcostabe/Desktop/PRODUTO REEF DESKTOP/index.html"
```
Ou inicie um servidor local:
```bash
cd "/Users/gcostabe/Desktop/PRODUTO REEF DESKTOP"
python3 -m http.server 8080
```
Acesse em: `http://localhost:8080`

---

© 2026 NTT DATA Brasil • Material confidencial e executivo.

---

## 🎯 Gênese do Sistema & Motivação Real: Caso MAPFRE

O desenvolvimento do **AXET-NeuralGraph 3D** nasceu de um desafio concreto e de altíssima urgência na **MAPFRE**:
* **O Volume do Acervo:**
  * **+1.000 horas de vídeos** contendo navegação em telas operacionais de sistemas legados de seguros, cursos de capacitação técnica, procedimentos de subscrição de apólices e regulação de sinistros.
  * **+2.000 documentos técnicos e funcionais** de especificação, modelos de dados e arquitetura do core de seguros (**Reef.core**).
* **A Motivação Central:**
  * Ter um **sistema ultra-rápido** para processamento e indexação massiva de milhares de arquivos corporativos e, especialmente, dos vídeos da Mapfre com sincronização entre **captura visual de telas (OCR multimodal)** e **transcrição contínua de voz (Whisper int8 local)**.
  * Inviabilidade técnica e regulatória de usar soluções em nuvem aberta (risco de vazamento de telas sensíveis, custos astronômicos em tokens e latência insustentável de upload de terabytes).
* **A Entrega:**
  * Um motor desktop em Tauri v2 (Rust) capaz de realizar ingestão local paralela, gerar o pacote comprimido e auditável **.qpack**, e entregar respostas com anclagem canônica e visualização neuroanatômica 3D em menos de 2 segundos.
