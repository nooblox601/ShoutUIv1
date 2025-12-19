# ShoutUI – Agent-to-User Interface

**ShoutUI** is an open-source project that defines a declarative format for agent-generated user interfaces, along with renderers that allow agents to generate, update, and control rich UIs safely across platforms.

ShoutUI enables agents to “speak UI” using structured data instead of executable code.

---

## ⚠️ Status: Early Stage Public Preview

> **Version:** v0.8  
> ShoutUI is in public preview. The specification and implementations are functional but still evolving. Breaking changes may occur as we move toward a stable v1.0.

---

## ✨ Overview

Generative AI is excellent at producing text and code, but agents often struggle to present **interactive, structured user interfaces**, especially when running remotely or across trust boundaries.

**ShoutUI** solves this by introducing a **declarative JSON-based UI protocol**:

- Agents describe *what* the UI should be
- Clients decide *how* to render it using native components

This makes agent-generated UIs:

- ✅ **Safe like data**
- 🚀 **Expressive like code**
- 🔁 **Incrementally updateable**
- 🌍 **Cross-platform**

---

## 🧠 Core Principles

### 🔐 Security First
- No arbitrary code execution
- Agents can only reference **pre-approved UI components**
- Full control remains with the client application

### 🤖 LLM-Friendly
- Flat component lists with ID references
- Designed for incremental updates and streaming
- Easy for LLMs to generate and modify

### 🧩 Framework-Agnostic
- One JSON payload → multiple platforms
- Works with Web, Flutter, and other UI frameworks
- Clean separation between UI description and UI implementation

### 🛠 Flexibility
- Open registry pattern for custom components
- Support for secure wrappers and sandboxed content
- Developers enforce their own trust and security policies

---

## 📦 Use Cases

- **Dynamic Forms**  
  Context-aware forms generated during a conversation

- **Remote Sub-Agents**  
  Specialized agents returning UI payloads to a main interface

- **Adaptive Workflows**  
  Dashboards, approvals, and visualizations generated on demand

---

## 🏗 Architecture

ShoutUI separates **UI generation** from **UI execution**:

1. **Generation**  
   An agent produces a `ShoutUI Response` (JSON)

2. **Transport**  
   Payload is sent via a supported protocol

3. **Resolution**  
   Client-side ShoutUI Renderer parses the payload

4. **Rendering**  
   Abstract components are mapped to native UI widgets

---

## 🔗 Ecosystem

ShoutUI is designed to integrate easily with existing systems:

- **LLMs:** Any model capable of structured JSON output
- **Transports:** Compatible with multiple agent communication protocols
- **Clients:** Web, mobile, or desktop applications

---

## 🚀 Getting Started

### Prerequisites

- Node.js (for web clients)
- Python (for agent examples)
- An API key for your preferred LLM provider

### Basic Steps

1. Clone the repository  
2. Configure your environment variables  
3. Run the agent backend  
4. Run the client renderer  

Exact steps depend on the renderer and platform you choose.

---

## 🗺 Roadmap

- Spec stabilization → **v1.0**
- More official renderers (React, mobile, desktop)
- Additional transport layers (REST, etc.)
- Support for more agent frameworks

---

## 🤝 Contributing

ShoutUI is licensed under **Apache 2.0**.

Contributions are welcome:
- Issues
- Feature requests
- Renderer implementations
- Documentation improvements

See `CONTRIBUTING.md` for details.

---

## 📄 License

Apache License 2.0  
See `LICENSE` for more information.

