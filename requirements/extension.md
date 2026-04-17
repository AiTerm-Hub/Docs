# AiTerm: Full Project Requirements

## 1. Translation Functionality

### Language Selection
* **UI Placement:** Language selection buttons are located below the text input and translation output blocks.
* **Selection Menu:** * Clicking a language button opens a selection window with available languages.
    * Languages are displayed in a single column with a vertical scrollbar.
    * The window features a close button (X icon).
    * **Visual Feedback:** The close button changes style on hover (white icon with border).
    * **Auto-Close:** The selection window closes automatically once a language is selected.

### Input & Output Logic
* **Manual Input:** Users can type or paste text into the input field.
* **Auto-Detection:** The source language is detected automatically after text entry.
* **Manual Override:** Users can manually change the detected source language.
* **Translation Display:** Translated text appears in the designated output field once the process is complete.

### Interaction Elements
* **Translate Button:**
    * **Action:** Triggers the translation and fetches additional data.
    * **Visuals:** The button is red.
    * **States:** The button only exists/is visible during the "processing/thinking" state.
* **Cancel Button:**
    * **Context:** During the translation process, a "Cancel" button replaces the "Language Swap" button.
* **Language Swap (Reverse) Button:**
    * **Action:** Swaps the source and target languages.
    * **Data Handling:** The text content in both fields is also swapped.

---

## 2. Advanced Linguistic Analysis (Linguistic Insights)

After translation, the following data must be displayed below the main blocks:
* **CEFR Level:** Proficiency level (A1 to C2).
* **Usage Frequency:** A scale from 1 to 10.
* **Contextual Data:** Synonyms, Examples, and Dictionary Explanations.

### Interaction with Insights
* **Display Format:** Examples, Synonyms, and Explanations are placed in separate UI blocks.
* **Navigation:** Users can switch between these blocks using navigation arrows (Left/Right).
* **Translation of Insights:** Users can translate the provided examples/synonyms into either the Input or Output language by clicking the respective language flag.

---

## 3. UI/UX & Animations

### Button Effects
* **Translate Button:** Response animation on click (blue outline and slight upward movement).
* **Language Selection Buttons:** Hover feedback (darker background shade).
* **Navigation Arrows:** Hover feedback (background fill) and click animation (vibration/shake effect).
* **Language List:** Hover highlighting for individual language items.

### Window & Content Animations
* **Selection Window:** Smooth "slide-in" effect.
    * **Input Language Window:** Slides from Left to Right; closes from Right to Left.
    * **Output Language Window:** Slides from Right to Left; closes from Left to Right.
* **Dynamic Data Rendering:** * **CEFR Level:** Counts up from A1 to the target level, ending with a "pop" animation (quick scale-up with blue background).
    * **Usage Frequency:** Counts up from 1 to the target value, accompanied by a circular progress fill and a "pop" animation.
    * **Text Content (Examples/Synonyms/Explanations):** Smooth fade-in appearance.
    * **Block Switching:** A "sliding page" animation when switching between examples, synonyms, and explanations.

---

## 4. Performance & Caching

* **Local Storage:** All translated text and corresponding linguistic data must be cached locally.
* **Instant Recall:** If a previously translated text is entered again, the translation and all associated information must be displayed instantly from the cache.

---

## 5. Error Handling & Validation

* **Missing Target:** Show a notification if the target language is not selected.
* **Empty State:** The translation process does not trigger if the input field is empty.
* **Matching Languages:** If the Input and Output languages are identical, only one flag/language icon is displayed to the user.
