# Gemma 3

An AI model for efficient local use and fine-tuning.

---

## Model

This project requires one large model file, which cannot be included directly due to size:

| Model              | Description          | Download Link                                                                                      |
|--------------------|----------------------|--------------------------------------------------------------------------------------------------|
| Gemma 3 model  | Core language model weights | [Download here](https://drive.google.com/file/d/1zPO4PN7q3z-qn49Pl0Ddd6gD_bwrbwMj/view?usp=drive_link) |

---

## Setup

1. Clone the repository:

```bash
git clone https://github.com/ouamy/gemma.git
cd gemma
```

2. Download the model file from the link above and place it in the `models/` directory:

```bash
gemma/
└── models/
    └── gemma-3-1b-it-Q4_K_M.gguf
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
build/bin/llama-server -m models/gemma-3-1b-it-Q4_K_M.gguf
```

This will start the server on:
```bash
http://127.0.0.1:8080
```
