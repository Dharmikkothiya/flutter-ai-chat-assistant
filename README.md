# 🤖 Flutter AI Chat Assistant (MVP)

A production-ready, feature-rich **AI Mobile Assistant** built with **Flutter**, **Riverpod**, and **Material 3**. Designed for high-performance agentic workflows with real-time streaming, multi-provider LLM routing, long-term memory, modular agent tools, and offline-first state synchronization.

---

## 🌟 Highlights

- **⚡ Real-Time Streaming Responses:** Smooth, token-by-token streaming chat powered by Server-Sent Events (SSE) and resilient chunk parsers.
- **🧠 Multi-Provider LLM Engine:** Seamlessly switch between **OpenAI**, **OpenRouter**, **InferHub**, **Z.AI**, or any custom OpenAI-compatible endpoint.
- **📚 Live Model Catalog:** Dynamic model discovery with search, category filtering, context length indicators, and pricing tiers.
- **💾 Long-Term Memory & Context Engine:** Intelligent conversation indexing, contextual memory injection, and session sandboxing.
- **🛠️ Modular Agent & Tool Execution:** In-app browser automation, sandboxed JavaScript runtime, and extensible skill sets (Web3, scraping, automation).
- **🔒 Privacy & Biometric Security:** Secure local storage (`flutter_secure_storage`), IP guard, and biometric authentication (Fingerprint / Face ID lock gate).
- **🎨 Sleek Cyber Dark UI:** Built with Flutter Material 3, custom electric-indigo/cyan accents, and responsive layout for all screen sizes.
- **🏗️ Clean Architecture:** Strictly decoupled domain models, service abstractions, Riverpod dependency injection, and offline-first persistence.

---

## 🏛️ Architecture Overview

The project adheres to Clean Architecture principles, ensuring scalability, maintainability, and testability:

```
lib/
├── di.dart                   # Central Riverpod Dependency Injection
├── main.dart                 # Application bootstrap & lifecycle management
├── l10n/                     # Localization & multi-language support
├── models/                   # Immutable domain models (Chat, Agent, Model, Preset)
├── services/                 # Core business logic & integrations
│   ├── agent_controller.dart # Central agent loop & tool orchestration
│   ├── llm_client.dart       # Streaming HTTP & multi-provider client
│   ├── model_catalog.dart    # Live model discovery and fetching
│   ├── memory_repository.dart# Persistent long-term memory store
│   ├── js_runtime.dart       # Sandboxed JS tool runner
│   ├── browser_automation.dart# Webview-based browser automations
│   └── app_lock_service.dart # Biometric & secure PIN lock gate
└── ui/                       # Presentation layer
    ├── screens/              # Full-page screens (Home, Chat, Settings, Skills, etc.)
    ├── widgets/              # Reusable UI components (MessageBubble, Composer, etc.)
    └── theme.dart            # Material 3 dynamic themes & color palettes
```

---

## 🚀 Getting Started

### Prerequisites

- [Flutter SDK](https://flutter.dev/docs/get-started/install) (`>= 3.13.5`)
- Android Studio / VS Code with Flutter & Dart extensions
- Android SDK (API Level 23+ recommended)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Dharmikkothiya/flutter-ai-chat-assistant.git
   cd flutter-ai-chat-assistant
   ```

2. **Install dependencies:**
   ```bash
   flutter pub get
   ```

3. **Run on connected device or emulator:**
   ```bash
   flutter run
   ```

---

## ⚙️ Configuration & API Setup

1. Open the app and navigate to **Settings** ⚙️ -> **Providers & API Keys**.
2. Add your API key for your preferred provider:
   - **OpenRouter** (Recommended for 100+ models): `https://openrouter.ai/`
   - **OpenAI**: `https://platform.openai.com/`
   - **Custom Endpoint**: Point to any local or self-hosted LLM (Ollama, vLLM, LM Studio).
3. Select your default model from the **Live Model Catalog** and start chatting!

---

## 🧪 Testing & Code Quality

Run the comprehensive unit, widget, and integration test suite:

```bash
# Run unit & widget tests
flutter test

# Run code analysis
flutter analyze
```

---

## 🛠️ Tech Stack & Libraries

- **Framework:** [Flutter](https://flutter.dev) (Dart 3)
- **State Management:** [flutter_riverpod](https://pub.dev/packages/flutter_riverpod)
- **Networking:** [http](https://pub.dev/packages/http)
- **Markdown Rendering:** [flutter_markdown](https://pub.dev/packages/flutter_markdown)
- **Local Persistence:** [shared_preferences](https://pub.dev/packages/shared_preferences) & [flutter_secure_storage](https://pub.dev/packages/flutter_secure_storage)
- **Biometric Auth:** [local_auth](https://pub.dev/packages/local_auth)
- **Webview & Sandbox:** [flutter_inappwebview](https://pub.dev/packages/flutter_inappwebview)
- **Speech-to-Text:** [speech_to_text](https://pub.dev/packages/speech_to_text)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
