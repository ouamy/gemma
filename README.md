# StarCoder

An AI model for code generation and understanding.

---

## Model

This project requires one large model file, which cannot be included directly due to size:

| Model              | Description          | Download Link                                                                                      |
|--------------------|----------------------|--------------------------------------------------------------------------------------------------|
| StarCoder model  | Core language model weights | [Download here](https://drive.google.com/file/d/11EO-25ZD39UwR8F8UnyTKQBYRPUjpGz5/view?usp=drive_link) |

---

## Setup

1. Clone the repository:

```bash
git clone https://github.com/ouamy/starcoder.git
cd starcoder
```

2. Download the model file from the link above and place it in the `models/` directory:

```bash
starcoder/
└── models/
    └── starcoderbase-1b.Q4_K_M.gguf
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
    -m models/starcoderbase-1b.Q4_K_M.gguf
```

This will start the server on:
```bash
http://127.0.0.1:8080
```
