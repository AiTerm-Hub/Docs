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

## 2. Functional Requirements

### Text Interaction
1. **Selection Trigger:** When a user highlights text on any webpage, a small AiTerm icon or a tooltip should appear near the cursor.
2. **Instant Translation:** Clicking the icon or using a hotkey (e.g., Alt + T) must automatically open the popup with the pre-filled translation and analysis.

### API Communication
* The extension must send a POST request to the backend with the selected text and language parameters.
* While waiting for the response, a smooth loading animation (spinner or skeleton) must be shown in the analysis module.
* **Error Handling:** If the API is unavailable or the internet is disconnected, a user-friendly error message must be displayed instead of a blank screen.

---

## 3. UI/UX & Design Constraints

* **Theme:** Strict Dark Mode (Hex codes to be defined in styles.md).
* **Effects:** * backdrop-filter: blur(10px) for the popup background.
    * Smooth micro-animations (0.3s duration) for opening the popup and switching languages.
* **Responsive:** The popup must have a fixed width (e.g., 350px) but adjust its height dynamically based on the content length.

---

## 4. User Flow (The "Happy Path")
1. **User** highlights the word "Resilient" on an English news site.
2. **User** presses the AiTerm icon.
3. **System** detects English, translates to Ukrainian, and identifies the level as C1.
4. **User** sees the translation, synonyms, and 2 examples of usage in the popup.
