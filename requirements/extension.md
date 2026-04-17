# AiTerm: Chrome Extension Requirements

This document outlines the functional and visual requirements for the AiTerm browser extension.

---

## 1. Main Interface (Popup)

The popup is the primary interaction point for the user. It must follow a minimalist design with a dark theme and modern UI elements.

### Translation Module
* **Input Zone:** A multi-line text area where users can type or paste source text.
* **Output Zone:** A read-only text area that displays the translated result. This area should have a subtle background distinction to indicate it is non-editable.
* **Language Selection:** Two dropdown menus positioned below the text zones:
    * **Left Dropdown:** Source language (Default: Auto-detect).
    * **Right Dropdown:** Target language (Default: User's preferred language).

### AI Analysis Module (Linguistic Insights)
After a successful translation, the extension must fetch and display the following data from the backend:

| Feature | Description | Range/Format |
| :--- | :--- | :--- |
| **CEFR Level** | Difficulty level of the word/phrase | A1, A2, B1, B2, C1, C2 |
| **Usage Frequency** | How common the word is in daily speech | 1 to 10 scale |
| **Synonyms** | List of similar words | Comma-separated list |
| **Examples** | Real-world usage sentences | Numbered list |
| **Explanation** | Dictionary-style definition | Short paragraph |

---
