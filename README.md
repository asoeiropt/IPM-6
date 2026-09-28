# **SmartGlycoAI** 🧬📱

*EN [English Version](#english) | PT [Versão em Português](#português)*

---

## <a name="english"></a> EN English

Welcome to the **SmartGlycoAI** repository. This project is a robust, cross-platform mobile application built with the **Flutter** framework. This initial commit establishes the foundational architecture, including strict static analysis rules and highly optimized native integrations for both Android and iOS environments.

### **📖 Table of Contents**
1. [Tech Stack](#tech-stack)
2. [Deep Dive: Repository Architecture](#deep-dive-repository-architecture)
3. [Prerequisites & Setup](#prerequisites--setup)
4. [Build & Run Instructions](#build--run-instructions)

### **🛠 Tech Stack**
*   **Framework:** Flutter
*   **Language:** Dart (Frontend/Logic), Kotlin (Android Native), Swift (iOS Native)
*   **Build System:** Gradle (Kotlin DSL `build.gradle.kts`), Xcode Build System

### **📂 Repository Architecture**
This initial commit contains the structural scaffolding required to build and deploy the app.

#### **1. Root Level & Dart Configuration**
*   `smart_glyco_ai/`: Root project directory.
*   `analysis_options.yaml`: Enforces strict Dart static analysis and linting rules to maintain code health.
*   `devtools_options.yaml`: Configures the Flutter DevTools environment for performance profiling and debugging.

#### **2. Android Native Module (`android/`)**
Fully configured for modern Android development utilizing Kotlin Script (KTS).
*   **Build & Gradle:**
    *   `build.gradle.kts` & `app/build.gradle.kts`: Modern Gradle configuration files using Kotlin DSL.
    *   `settings.gradle.kts`: Defines project modules and repositories.
*   **Manifests by Build Profile (`app/src/`):**
    *   `debug/AndroidManifest.xml`: Includes permissions required only during debugging (e.g., internet for hot-reload).
    *   `main/AndroidManifest.xml`: The core manifest detailing the app package, hardware permissions, and the `MainActivity`.
    *   `profile/AndroidManifest.xml`: Configured specifically for performance profiling mode.
*   **Source Code:**
    *   `.../kotlin/com/example/smart_glyco_ai/MainActivity.kt`: The Kotlin entry point that boots the FlutterEngine.
*   **UI Resources (`app/src/main/res/`):**
    *   **Drawables:** `drawable-hdpi` through `drawable-xxxhdpi` and `drawable-v21` contain the splash screen (`splash.png`) and `launch_background.xml` to ensure a seamless launch experience across all pixel densities.
    *   **Mipmaps:** `mipmap-hdpi` through `mipmap-xxxhdpi` store the application launcher icons (`ic_launcher.png`, `launcher_icon.png`).
    *   **Values:** `values-night` and `values-night-v31` provide dynamic theming, including Dark Mode support and Android 12+ API specific styles (`styles.xml`).

#### **3. iOS Native Module (`ios/`)**
Fully scaffolded for compilation in Xcode.
*   **Project & Workspace:**
    *   `Runner.xcodeproj` / `Runner.xcworkspace`: Xcode project structures and shared scheme data (`Runner.xcscheme`).
*   **Source Code:**
    *   `Runner/AppDelegate.swift`: Swift entry point that delegates application lifecycle events to the Flutter framework.
*   **Visual Assets (`Runner/Assets.xcassets/`):**
    *   `AppIcon.appiconset`: Contains precise icon resolutions required by Apple guidelines (from 20x20 to 1024x1024 across `@1x`, `@2x`, and `@3x` scales).
    *   `LaunchImage.imageset` & `LaunchBackground.imageset`: Setup for the native iOS splash screen transition.
*   **Flutter Integration (`Flutter/`):**
    *   `Debug.xcconfig` & `Release.xcconfig`: Connects Xcode's build phases to the Flutter SDK.

### **⚙️ Prerequisites & Setup**
Ensure your local environment is configured with:
*   **Flutter SDK:** `flutter doctor` must report no errors.
*   **Android Studio / IntelliJ:** Required for Android emulation and SDK tooling.
*   **Xcode:** Required for iOS compilation (macOS only).

### **🚀 Build & Run Instructions**
Run the following commands in the terminal at the root of the project:

    # Get all project dependencies
    flutter pub get

    # Run the app on an attached device or emulator
    flutter run

    # Build a release APK for Android
    flutter build apk --release

    # Build a release IPA for iOS
    flutter build ipa --release

---

## <a name="português"></a> PT Português

A **SmartGlycoAI** é uma aplicação móvel multiplataforma robusta, construída com a framework **Flutter**. Este *commit* inicial estabelece a arquitetura de base, incluindo regras estritas de análise de código e integrações nativas altamente otimizadas para ambientes Android e iOS.

### **📖 Índice**
1. [Tecnologias Utilizadas](#tecnologias-utilizadas)
2. [Análise Profunda: Arquitetura do Repositório](#análise-profunda-arquitetura-do-repositório)
3. [Pré-requisitos e Configuração](#pré-requisitos-e-configuração)
4. [Instruções de Execução](#instruções-de-execução)

### **🛠 Tecnologias Utilizadas**
*   **Framework:** Flutter
*   **Linguagem:** Dart (Frontend/Lógica), Kotlin (Nativo Android), Swift (Nativo iOS)
*   **Sistemas de Build:** Gradle (Kotlin DSL `build.gradle.kts`), Xcode Build System

### **📂 Arquitetura do Repositório**
Este *commit* inicial contém o esqueleto estrutural necessário para compilar a aplicação.

#### **1. Raiz do Projeto e Configuração Dart**
*   `smart_glyco_ai/`: Diretório raiz do projeto.
*   `analysis_options.yaml`: Aplica regras estritas de análise estática e *linting* do Dart para garantir a qualidade do código.
*   `devtools_options.yaml`: Configura o ambiente do Flutter DevTools para análise de desempenho e *debugging*.

#### **2. Módulo Nativo Android (`android/`)**
Configurado para o desenvolvimento Android moderno utilizando Kotlin Script (KTS).
*   **Build e Gradle:**
    *   `build.gradle.kts` & `app/build.gradle.kts`: Ficheiros modernos de configuração Gradle a usar Kotlin DSL.
    *   `settings.gradle.kts`: Define os módulos e repositórios do projeto.
*   **Manifestos por Perfil de Build (`app/src/`):**
    *   `debug/AndroidManifest.xml`: Inclui permissões necessárias apenas durante o *debugging* (ex: internet para o *hot-reload*).
    *   `main/AndroidManifest.xml`: O manifesto central que detalha o pacote, permissões de hardware e a `MainActivity`.
    *   `profile/AndroidManifest.xml`: Configurado especificamente para o modo de análise de desempenho (*profiling*).
*   **Código-Fonte:**
    *   `.../kotlin/com/example/smart_glyco_ai/MainActivity.kt`: O ponto de entrada em Kotlin que inicia o FlutterEngine.
*   **Recursos de Interface (`app/src/main/res/`):**
    *   **Drawables:** De `drawable-hdpi` a `drawable-xxxhdpi` e `drawable-v21`, contêm o ecrã de apresentação (`splash.png`) e `launch_background.xml` para garantir uma transição de ecrã fluída em qualquer densidade de píxeis.
    *   **Mipmaps:** De `mipmap-hdpi` a `mipmap-xxxhdpi`, armazenam os ícones da aplicação (`ic_launcher.png`, `launcher_icon.png`).
    *   **Values:** `values-night` e `values-night-v31` fornecem temas dinâmicos, incluindo suporte a Modo Escuro e estilos específicos para APIs Android 12+ (`styles.xml`).

#### **3. Módulo Nativo iOS (`ios/`)**
Estruturado para compilação no Xcode.
*   **Projeto e Workspace:**
    *   `Runner.xcodeproj` / `Runner.xcworkspace`: Estruturas do projeto Xcode e dados partilhados (`Runner.xcscheme`).
*   **Código-Fonte:**
    *   `Runner/AppDelegate.swift`: Ponto de entrada em Swift que delega os eventos de ciclo de vida da aplicação para a framework Flutter.
*   **Ativos Visuais (`Runner/Assets.xcassets/`):**
    *   `AppIcon.appiconset`: Contém as resoluções de ícones precisas exigidas pelas diretrizes da Apple (desde 20x20 a 1024x1024 em escalas `@1x`, `@2x` e `@3x`).
    *   `LaunchImage.imageset` & `LaunchBackground.imageset`: Ecrãs de apresentação e imagens de fundo para a sequência de lançamento no iOS.
*   **Configuração Flutter iOS (`Flutter/`):**
    *   `AppFrameworkInfo.plist`, `Debug.xcconfig`, `Release.xcconfig`: Definições de compilação que ligam o motor do Flutter ao processo de *build* do Xcode.

### **⚙️ Pré-requisitos e Configuração**
Garanta que o seu ambiente local está configurado com:
*   **Flutter SDK:** O comando `flutter doctor` não deve reportar erros.
*   **Android Studio / IntelliJ:** Necessário para emulação Android e ferramentas do SDK.
*   **Xcode:** Necessário para compilação iOS (exclusivo para macOS).

### **🚀 Instruções de Execução**
Execute os seguintes comandos no terminal, na raiz do projeto:

    # Obter todas as dependências do projeto
    flutter pub get

    # Correr a aplicação num dispositivo físico ou emulador
    flutter run

    # Compilar um APK de release para Android
    flutter build apk --release

    # Compilar um IPA de release para iOS
    flutter build ipa --release
