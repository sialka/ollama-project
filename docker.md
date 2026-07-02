#  🐑 Inteligência Artificial


## 🐋 Docker


### 📋 Interpretador

> Motor para processar os modelos

```bash
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

### 🗂️ Baixando os Modelos

Para baixar os modelos abaixo, o container ollama/ollama precisa estar ligado.

```bash
> Modelo llama2

$ docker exec -it ollama ollama run llama2

> Modelo gemma3

$ docker exec -it ollama ollama run gemma3

> Modelo gemma4

$ docker exec -it ollama ollama run gemma4
```

### 🖥️ Servidor

> Chat para utilizar os modelos

```bash
docker run -d -p 3000:8080 \
  -e OLLAMA_BASE_URL=http://host.docker.internal:11434 \
  -v open-webui:/app/backend/data \
  --name open-webui \
  --restart always \
  ghcr.io/open-webui/open-webui:main
  ```


### 🔥 Subindo o Servidor


Renomeio o llamafile-0.10.3 para llamafile.exe

Sintaxe do comando no terminal:

```bash
$ llamafile.exe --server --model <model>
```


🖼️ *No Windows*

Exemplo:

```bash
$ llamafile.exe --server --model qwen3-4b-thinking-2507.Q4_K_M.gguf
```

---