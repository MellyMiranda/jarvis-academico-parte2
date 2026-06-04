Este projeto é a continuação do Trabalho 1, adicionando:
- Active Recall
- Planejamento de estudos
- Geração de exercícios
- Avaliação do sistema

▶️ Execução
Opção 1: Abrir diretamente pelo Google Colab
Abrir o notebook no Google Colab (https://colab.research.google.com/drive/1IBEvt0nRNqTacGbdYXtIbsldAPQ92ak_?usp=sharing)
Executar todas as células do notebook
Abrir interface Gradio gerado ao final da execução

Opção 2: Executar localmente pelo GitHub
Abrir repositório no GitHub
Clicar em: Code -> Download ZIP
Extrair o arquivo .zip
Abrir Google Colab
Fazer upload do notebook: Trabalho_jarvis_academico.ipynb
Executar todas as células
Abrir interface Gradio gerado ao final da execução

OBS: LINK DO RELATÓRIO FINAL DO TRABALHO JARVIS - PARTE 1 E 2: https://docs.google.com/document/d/1HG90mNpIqZQhXMaeN-YlKC0AbsnUe9V3ayl3v730orQ/edit?usp=sharing

🤖 Ferramentas de IA Utilizadas
Gemini
ChatGPT

✅ Funcionalidades Implementadas (Trabalho 2)
📚 3.4 - Planejamento de estudos

O sistema agora combina automaticamente:
agenda acadêmica
lista de tarefas
materiais do RAG
Exemplos:
“Monte um plano de estudos para a prova”
“O que devo priorizar hoje?”
Funcionamento:
recuperação de contexto (RAG + agenda + tarefas)
geração de plano personalizado via LLM
resposta estruturada com prioridades

🧠 5. Melhoria de Aprendizado (ACTIVE RECALL)

O sistema implementa um modo interativo de aprendizagem baseado em:
✔ Active Recall (interativo)

O sistema:
gera uma pergunta automaticamente baseada no material
aguarda resposta do usuário
avalia a resposta
retorna feedback (correta / parcial / incorreta)
pode continuar o ciclo ou encerrar
🔁 Fluxo do Active Recall:
“Me teste sobre regressão logística”
→ sistema gera pergunta
usuário responde
→ sistema avalia
opções:
“mais uma” → nova pergunta
“encerrar” → finaliza teste

📌 Funcionalidades incluídas:
geração dinâmica de perguntas
avaliação automática com LLM
controle de sessão de teste
histórico de perguntas anteriores (evita repetição)

🧪 6. Avaliação do Sistema 

O sistema foi testado com 10 perguntas reais, incluindo:

consultas RAG
tarefas
agenda
planejamento de estudos
active recall
Estrutura da avaliação

Para cada pergunta:
pergunta realizada
documentos recuperados (RAG)
resposta gerada
classificação:
correta
parcialmente correta
incorreta

📊 7. Análise de Erros (NOVO)

Foram identificadas falhas como:

1. Erro de recuperação (RAG)
causa: chunks quebrando contexto
solução: melhorar overlap e chunk size
2. Ambiguidade de intenção
causa: linguagem natural do usuário
solução: melhorar classificador de tool calling
3. Respostas fora do contexto
causa: LLM ignorando parte do contexto recuperado
solução: reforçar prompt de grounding

🛠️ Tool Calling (melhorado)
O sistema mantém e expande o tool calling com LLM.

Ferramentas:
buscar_material_rag
listar_tarefa
adicionar_tarefa
concluir_tarefa
excluir_tarefa
listar_agenda
adicionar_evento
excluir_evento
planejar_estudos
gerar_exercicios
iniciar_teste
avaliar_resposta

📌 Destaque:
A decisão de ferramentas continua sendo feita pela LLM, com roteamento automático.


📂 Dataset (expansão)
Mantido o dataset anterior com: 10 documentos acadêmicos

🧠 Tecnologias Utilizadas (mantido + expandido)
Python
Gradio
FAISS
Sentence Transformers
OpenRouter API
Qwen
LangChain (apoio RAG)

💡 Diferenciais do Trabalho 2
Active Recall interativo
Avaliação automática de respostas
Geração dinâmica de perguntas
Controle de sessão de teste
Integração RAG + planejamento + aprendizagem

👨‍💻 Desenvolvido por
Melly Sabrina Araújo Miranda
