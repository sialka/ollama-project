#  🐑 Inteligência Artificial

## 💡 Instalando o Ollama


**Linux**

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

**Windows**

```bash
irm https://ollama.com/install.ps1 | iex
```

ou 

https://ollama.com/download/OllamaSetup.exe


## 🏷️ Principais Comandos

| **Sintaxe* | *Descrição* |
| :--- | :--- |
| ```ollama -v``` | Exibe a versão. |
| ```ollama pull <modelo>``` | Baixa o modelo. |
| ```ollama list``` | Lista os modelos. |
| ```ollama rm <name>``` | Remove o modelo. |
| ```ollama run <name>``` | Executa o modelo. |

## 🔥 Executando

```bash
$ OLLAMA_HOST=127.0.0.1:11435 ollama serve
``` 

## 📂 Baixando Modelos

Principais modelos do **Gemma 4**.

```bash
$ ollama pull gemma4:e2b
$ ollama pull gemma4:e4b
$ ollama pull gemma4:26b
$ ollama pull gemma4:31b
```
