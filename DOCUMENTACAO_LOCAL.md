# Documentação Técnica: Execução Local e Tradução (openGym)

Guia de referência rápida para manutenção e execução do projeto sem Docker e com localização em Português do Brasil (`pt-BR`).

---

## 1. Como Iniciar o Projeto Localmente

### A. Backend (API)
Abra um terminal na raiz do projeto:
```bash
PORT=3000 DATA_DIR=$(pwd)/data node --env-file=.env api/server.js
```
*Porta:* `3000` | *Health check:* [http://127.0.0.1:3000/api/health](http://127.0.0.1:3000/api/health)

### B. Frontend (Vite)
Abra outro terminal na pasta `frontend`:
```bash
cd frontend
npm run dev
```
*Porta:* `5173` | *URL da Aplicação:* [http://localhost:5173](http://localhost:5173)

---

## 2. Estrutura de Tradução (pt-BR)

* `.env`: Define `DEFAULT_LANG=pt-BR`.
* `frontend/index.html`: Shell inicial com `lang="pt-BR"`.
* `frontend/src/store/useStore.js`: Configurado com fallback de idioma `pt-BR` e migração automática.
* `frontend/src/lib/default-lang.js`: Resolução de idioma padrão priorizando `pt-BR`.
* `frontend/src/locales/pt-BR.js`: Dicionário completo de textos da interface.
* `frontend/src/exercise-names/pt-BR.js`: Tradução dos nomes de exercícios.
* `frontend/src/instr/pt-BR.js`: Instruções passo a passo de execução dos treinos.
