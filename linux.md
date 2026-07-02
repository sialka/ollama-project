#  🐑 Inteligência Artificial


##  🐧 Linux


### 🔬 Laboratório

Crie uma pasta e coloque os arquivos mencionados abaixo:

Exemplo: 

```
📂 Lab    
```


### 🖥️ Servidor

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


### 🗂️ Baixe os Modelos

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


### 🔥 Subindo o Servidor


Renomeio o llamafile-0.10.3 para llamafile.exe

Sintaxe do comando no terminal:

```bash
$ llamafile.exe --server --model <model>
```

```bash
$ chmod +x llamafile
$ .\llamafile --server --model qwen3-4b-thinking-2507.Q4_K_M.gguf
```

---