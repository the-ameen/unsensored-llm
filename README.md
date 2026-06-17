# Uncensored-LLM ⚡

**Uncensored-LLM** is a fully air-gapped, zero-dependency, plug-and-play Local AI environment designed to run seamlessly from your **local hard drive** or a **portable USB/SSD**. Developed and packaged by **[Mohd Ameen](https://github.com/the-ameen)**, it bypasses complex installations, executing large language models natively on your hardware with no internet required.

With a unified architecture, you can initialize your AI models once and choose to keep them on your system or carry them with you across Windows, macOS, and Linux PCs.

---

## 🚀 Core Features

* **Zero-Dependency Setup:** Ships with portable runtime configurations and isolated engine binaries. No system permissions, registry edits, or package managers required.
* **Cross-Platform Interoperability:** Uses an intelligent `Shared` volume system — download your heavy AI models *once*, and run them natively on Windows, macOS, Linux, or Android without duplication.
* **Ablated & Uncensored Models:** Pre-configured for cutting-edge uncensored and heretic fine-tuned models for completely unfiltered, raw interactions.
* **Local Web Interface:** Serves a blazing-fast, responsive dark-mode chat UI with real-time host CPU/RAM hardware utilization stats.
* **LAN Mobile Access:** Access the running AI engine from your phone or tablet on the same WiFi network without complex CORS configuration.
* **Hardware Accelerated:** Capitalizes on CPU instructions (AVX/AVX2), Apple Metal GPU accelerators, or NVIDIA CUDA dynamically depending on the host machine.

---

## 📂 Folder Architecture

The project is structured to strictly isolate operating system executables while securely unifying heavy model weights to save precious portable storage capacity.

```text
Uncensored-LLM/
 ├── 📁 Android    # Native Android (Termux) installers & launchers
 ├── 📁 Linux      # Native Ubuntu/Debian offline installers & launchers
 ├── 📁 Mac        # Native macOS offline installers & launchers
 ├── 📁 Windows    # Native Windows offline automatic UI menus
 └── 📁 Shared     # Unified Data System
      ├── 📁 bin         (Holds isolated executables: ollama-windows.exe, ollama-darwin...)
      ├── 📁 chat_data   (Houses cross-platform persistent conversation history)
      ├── 📁 models      (HuggingFace GGUF Weights & local database mapping)
      └── 📁 scripts     (Bootstrap and offline asset configuration utilities)
```

---

## 🧠 Curated AI Model Catalog

The installer supports downloading the highest-quality, locally operable uncensored models available on the open-source market today:

| Model Name | Size | Profile Type | Description |
| :--- | :--- | :--- | :--- |
| **Gemma 2 2B Abliterated** | ~1.6 GB | Uncensored | **Recommended for all.** Extremely fast, highly competent for its size. |
| **Gemma 4 E4B Ultra Heretic** | ~5.34 GB | Uncensored | Complies aggressively with all user queries regardless of subject matter. |
| **Qwen 3.5 9B Uncensored** | ~5.2 GB | Uncensored | Strong reasoning and instruction-following capability. |
| **NemoMix Unleashed 12B** | ~7.0 GB | Uncensored | Heavyweight reasoning and deep context processing. |
| **Dolphin 2.9 Llama 3 8B** | ~4.9 GB | Uncensored | Highly versatile and popular uncensored instruct model. |
| **Phi-3.5 Mini 3.8B** | ~2.2 GB | Standard | Fast, lightweight reasoning and technical/coding assistant. |

> **Custom Models:** You can place any standard `.gguf` model from HuggingFace into the `Shared/models/` directory, configure a Modelfile, and run it natively.

---

## ⚙️ Quick Start Guide

### Step 1: Initialize the Engine
Navigate into the folder matching your current host operating system and run the installer:
* **macOS:** Open Terminal, run `Mac/install.command`.
* **Windows:** Double-click `Windows/install.bat`.
* **Linux:** Run `bash Linux/install.sh`.
* **Android (Termux):** Open Termux and run `bash Android/install.sh`.

### Step 2: Download AI Models
Choose a model during the installation wizard. If you are offline, you can manually place downloaded GGUF files directly inside the `Shared/models/` directory.

### Step 3: Launch
Open the respective OS folder and run the start script:
* **macOS:** `Mac/start.command`
* **Windows:** `Windows/start-fast-chat.bat`
* **Linux:** `bash Linux/start.sh`
* **Android:** `bash Android/start.sh`

The engine will spin up securely in the background, and your default web browser will automatically open the locally-served Chat UI on `http://localhost:3333`.

---

## 📱 LAN Mobile Access

To access the AI engine from your phone or tablet on the same WiFi network:
1. Ensure your host machine running the `start` script and your mobile device are on the exact same WiFi network.
2. The server terminal will display your local network address (e.g., `http://192.168.1.15:3333`).
3. Enter this address in your mobile browser. Queries will be routed and executed locally on the host machine.

---

## 🛠️ Troubleshooting

* **Script instantly closes on Windows:** Right-click the `.bat` file and select "Run as Administrator", or run the script manually from a PowerShell/CMD window.
* **"Ollama Engine Not Found" or "Missing Runtime":** Make sure you run the setup installer (`install.command` / `install.bat`) first before attempting to start the chat server.
* **Slow Inference Speeds:** The model might exceed your available system RAM/VRAM. Re-run the installer and select the lightweight **Gemma 2 2B Abliterated** model, which performs rapidly even on older machines.

---

## ⚖️ Disclaimer & License

This project is built for uncompromising computational freedom. By utilizing ablative models, the system will not moralize, lecture, or refuse prompts. Please use responsibly.

Project packaged and maintained by [Mohd Ameen](https://github.com/the-ameen). Licensed under the MIT License.
