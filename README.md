# DeepSeek Coder

A small, instruction-tuned AI model for clean code generation.

---

## Model

This project requires one large model file, which cannot be included directly due to size:

| Model              | Description          | Download Link                                                                                      |
|--------------------|----------------------|--------------------------------------------------------------------------------------------------|
| DeepSeek Coder model  | Core language model weights | [Download here](https://drive.google.com/file/d/1VjSNIJzmBmeX2BOPor_B2dAgj_SjdrpR/view?usp=drive_link) |

---

## Setup

1. Clone the repository:

```bash
git clone https://github.com/ouamy/deepseek.git
cd deepseek
```

2. Download the model file from the link above and place it in the `models/` directory:

```bash
deepseek/
└── models/
    └── deepseek-coder-1.3b-instruct.Q2_K.gguf
```

3. Copy all the .so files to /usr/local/lib and run ldconfig

```bash
sudo cp build/bin/lib*.so /usr/local/lib/
sudo ldconfig
```

---

## Run

Start the server with the model:
```bash
build/bin/llama-server \
    -m models/deepseek-coder-1.3b-instruct.Q2_K.gguf
```

This will start the server on:
```bash
http://127.0.0.1:8080
```
