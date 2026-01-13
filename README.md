# bramble-editor

A lightweight, browser-based code editor with live preview capabilities. Bramble Core provides syntax highlighting, linting, and formatting while outputting clean HTML, CSS, and JavaScript.

## 🗺️ System Architecture

```mermaid
flowchart TD
    subgraph UserInterface["💻 USER INTERFACE"]
        Editor["✏️ Code Editor"]
        Preview["👁️ Live Preview"]
        FileTree["📁 File Tree"]
    end

    subgraph Core["⚙️ BRAMBLE CORE"]
        Parser["🔍 Code Parser"]
        Syntax["🎨 Syntax Highlighting"]
        Linter["✅ Linter"]
        Formatter["📝 Formatter"]
    end

    subgraph Output["📤 OUTPUT"]
        HTML["🌐 HTML Render"]
        CSS["🎯 CSS Styles"]
        JS["⚡ JavaScript"]
    end

    Editor --> Core
    FileTree --> Editor
    Core --> Output
    Parser --> Syntax
    Parser --> Linter
    Syntax --> Formatter
    Output --> Preview

    style UserInterface fill:#FFF9C4,color:#000
    style Core fill:#40C4D4,color:#000
    style Output fill:#FFF9C4,color:#000
```
