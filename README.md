# LangChain

Personal practice repo working through core LangChain concepts: models, prompts, and structured output.

## Structure

| Folder | Demonstrates |
|---|---|
| `LANGCHAIN MODELS/` | Base `LLM`, `ChatModel`, and embeddings across OpenAI, Anthropic, Google, and Hugging Face — see its own [README](LANGCHAIN%20MODELS/README.md) |
| `PROMPTS/` | `PromptTemplate`/`load_prompt`, `ChatPromptTemplate` with `MessagesPlaceholder`, a Streamlit research-summary UI, and a terminal chatbot with history |
| `STRUCTURED OUTPUT/` | Constraining model output via `TypedDict`, Pydantic, and raw JSON Schema with `with_structured_output` |

## Setup

```bash
python -m venv venv
venv\Scripts\activate        # or `source venv/bin/activate` on macOS/Linux
```

Each folder has its own `.env` (gitignored) with the API keys its scripts need, e.g.:

```
GOOGLE_API_KEY=...
OPENAI_API_KEY=...
ANTHROPIC_API_KEY=...
HUGGINGFACEHUB_API_TOKEN=...
```

Scripts within `PROMPTS/` share one Gemini client via `model_loader.py` instead of each re-initializing it.

## Why this exists

Learning/reference repo — each script isolates one LangChain concept rather than building a single end-to-end application.
