# **SmartGlycoAI**

Repositório inicial e estrutura base para o desenvolvimento da aplicação **SmartGlycoAI**, uma solução multiplataforma criada com a framework **Flutter**.

## **Descrição**

Este repositório contém o código-fonte inicial da aplicação SmartGlycoAI. O projeto junta a flexibilidade do Flutter para a interface do utilizador com as configurações nativas necessárias para a execução otimizada em dispositivos móveis, focando-se nesta fase inicial na plataforma Android.

## **Estrutura do Commit Inicial**

Abaixo encontra-se a organização dos principais ficheiros e diretórios disponibilizados no commit inicial do projeto:

| Caminho / Ficheiro | Descrição |
| :--- | :--- |
| `smart_glyco_ai/` | Diretório raiz e principal do projeto Flutter. |
| `analysis_options.yaml` | Ficheiro de configuração para o linter do Dart e regras de análise estática do código. |
| `android/` | Diretório com a estrutura e configurações nativas específicas para a plataforma Android. |
| `android/app/build.gradle.kts` | Ficheiro de configuração do build do módulo da app, escrito em Kotlin Script (KTS). |
| `android/app/src/main/AndroidManifest.xml` | Manifesto principal onde estão declaradas as permissões, componentes e configurações base da app Android. |
| `android/app/src/main/kotlin/.../MainActivity.kt` | Ficheiro fonte em Kotlin que representa a Activity principal e ponto de entrada nativo da aplicação. |
| `android/app/src/main/res/` | Diretório de recursos visuais e estáticos do projeto Android. |

### **Recursos Nativos (`android/app/src/main/res/`)**
O diretório de recursos está organizado em subpastas otimizadas para diferentes densidades de ecrã e versões do sistema operativo:
*   **`drawable/` e variações** (`drawable-hdpi`, `drawable-mdpi`, `drawable-xhdpi`, `drawable-xxhdpi`, `drawable-xxxhdpi`, `drawable-v21`):
    *   Contêm os ativos do ecrã de lançamento e transição da app.
    *   Ficheiros incluídos: `background.png`, `launch_background.xml` e o ecrã de carregamento `splash.png`.
*   **`mipmap/` e variações** (`mipmap-hdpi`, `mipmap-mdpi`, `mipmap-xhdpi`, `mipmap-xxhdpi`, `mipmap-xxxhdpi`):
    *   Contêm os ícones oficiais da aplicação otimizados para todas as resoluções de ecrã suportadas.
    *   Ficheiros incluídos: `ic_launcher.png` e `launcher_icon.png`.

## **Notas de Desenvolvimento**
*   **Kotlin Script (KTS):** A configuração de build da aplicação Android utiliza Kotlin Script (`build.gradle.kts`), seguindo as práticas e recomendações mais recentes do ecossistema Android.
*   **Estrutura Padrão Flutter:** O projeto adota a arquitetura standard do Flutter para integração com a plataforma nativa, garantindo escalabilidade e facilidade na adição de dependências futuras.
