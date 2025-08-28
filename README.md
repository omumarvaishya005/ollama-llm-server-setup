# Ollama Local LLM Server Setup

A simple guide to setting up a local Ollama LLM server. This repository explains how to pull models, start the server, and interact with it via API. Perfect for developers who want a lightweight, local environment to experiment with large language models without GPU dependency.

---

## Features

- Pull and manage Ollama models
- Run a local LLM server
- Interact via HTTP API
- CPU-only or GPU-enabled usage

---

## Requirements

- Linux, macOS, or Windows
- Docker (for Docker-based setup)
- Python 3.10+ (optional if using Python scripts)
- Internet connection (for model download)

---

## Quick Setup

### 1. Install Ollama

Follow the instructions from [Ollama website](https://ollama.com/) to install the CLI.

### 2. Pull a Model

```bash
ollama pull llama3:8b
```
This downloads the llama3:8b model to your local system.
### 3. Start the Server

```bash 
ollama serve
```

By default, the server runs at:

http://localhost:11434

### 4. List Available Models

```bash
ollama list
```

### 5. Generate Text Using API

Send a request to the server using curl:

```bash
curl http://localhost:11434/api/generate -d '{
  "model": "llama3:8b",
  "prompt": "Hello from ApplyWise!"
}'
```

You will receive streaming responses from the model.
### Notes

    You can run multiple models by pulling them and specifying the model name in the API request.

    Ollama handles model caching locally in ~/.ollama by default.

    CPU-only setups are fully supported. GPU usage requires Docker with NVIDIA runtime or system GPU drivers.

### References

    Ollama Official Website

Ollama Documentation
License

This repository is open for personal or educational use. Adapt and share as needed.


