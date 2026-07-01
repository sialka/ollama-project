#  🐑 IA Local

## 🐋 Docker

📋 *Interpretador*

> Motor para processar os modelos

```bash
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

🗂️ *Modelos*

Para baixar os modelos abaixo, o container ollama/ollama precisa estar ligado.

```bash
> Modelo llama2

$ docker exec -it ollama ollama run llama2

> Modelo gemma3

$ docker exec -it ollama ollama run gemma3

> Modelo gemma4

$ docker exec -it ollama ollama run gemma4
```

🖥️ *Servidor*

> Chat para utilizar os modelos

```bash
docker run -d -p 3000:8080 \
  -e OLLAMA_BASE_URL=http://host.docker.internal:11434 \
  -v open-webui:/app/backend/data \
  --name open-webui \
  --restart always \
  ghcr.io/open-webui/open-webui:main
  ```

---

##  🕹️ Local


🔬 *Laboratório*

Crie uma pasta e coloque os arquivos mencionados abaixo:

Exemplo: 

```
📂 Lab    
```


🖥️ *Servidor*

> Baixando o servidor

Acesse a url https://github.com/mozilla-ai/llamafile

Em Release localize:

```
llamafile v0.10.3 (ou superior)
```

Em Assets baixe o arquivo:

```
llamafile-0.10.3 (ou superior)
```

```
📂 Lab
    └─ llamafile-0.10.3
```


 ├─
 └─


🗂️ *Modelos*

Acesse https://huggingface.co/ e em Libraries procure por GGUF.

Pequise o modelo que tem interesse exemplos: 

- qween3
- gemma3 
- gemma4

Depois em 'Files and versions' procure o arquivo com a extesão .gguf e baixe o modelo.

Exemplos:

- qwen3-4b-thinking-2507.Q4_K_M.gguf
- gemma-3-1B-it-GLM-4.7-Flash-Heretic-Uncensored-Thinking_F16
- gemma-4-E2B_q4_0-it

```
📂 Lab
    ├─ llamafile-0.10.3
    ├─ qwen3-4b-thinking-2507.Q4_K_M.gguf
    ├─ gemma-3-1B-it-GLM-4.7-Flash-Heretic-Uncensored-Thinking_F16
    └─ gemma-4-E2B_q4_0-it
```



🔥 *Execução*


Renomeio o llamafile-0.10.3 para llamafile.exe

Sintaxe do comando no terminal:

$ llamafile.exe --server --model <model>


🖼️ *No Windows*

Exemplo:

```
$ llamafile.exe --server --model qwen3-4b-thinking-2507.Q4_K_M.gguf
```

🐧 *No Linux*

```
$ chmod +x llamafile
$ .\llamafile --server --model qwen3-4b-thinking-2507.Q4_K_M.gguf
```

---