# Requirements

## Feature: Translation

### Language Selection
* Below the text input and translation blocks – there must be language selection buttons.

### Text Input Block
* User can enter text manually.
* Language is determined automatically after text entry.
* User can manually change the detected language.

### Translation Block
* User must choose a translation language.
* Translated text is displayed in the corresponding field.

### Translation Button
* Clicking triggers the text translation.
* Translation must be displayed in the corresponding translation field.
* While waiting for the translation, a cancel button should appear instead of the swap button.
* The translation button must be red.
* The translation button should exist only during "thinking" (processing).

### Language Swap Button
* The button should swap the input and output languages.
* Text also swaps places.

### Language Selection Window
* After clicking, a window with a choice of available languages should appear.
* The window must have a close button (cross icon).
* Languages should be arranged as a column and have vertical scrolling with a scrollbar.

### Additional Information
* The following information should appear below after translation:
    * Language level (A1-C2).
    * Usage level (1-10).
    * Examples.
    * Synonyms.
    * Explanation.
* User must be able to translate the received information into 2 languages (Input language, output language).
* User can translate the information by clicking on the corresponding flag (Input language, output language).
* Examples, synonyms, and explanations should be in separate blocks.
* Examples, synonyms, and explanations must switch when the corresponding button is pressed (left arrow, right arrow).

### Animations
* The translation button must have a feedback animation upon clicking (Blue outline, moving slightly upwards).
* When hovering over the language selection button – buttons must have feedback (Darker color).
* The language selection window should slide out smoothly when the corresponding buttons are pressed.
* When clicking the button to select the **Input language** – the window should slide from left to right and close from right to left.
* When clicking the button to select the **output language** – the window should slide from right to left and close from left to right.
* When hovering over a language, the language should be highlighted.
* When a language is selected - the window should close according to the language selection button.
* When hovering over the cross icon of the language selection window – the cross must have feedback (white cross with an outline).
* The following information must appear and disappear exclusively with a smooth animation:
    * Language level (A1-C2) – count up from A1 with an end animation (fast increase with a blue background).
    * Usage level (1-10) - count up from 1 with an end animation (fast increase with a blue background) and a circle fill animation.
    * Examples (Soft appearance).
    * Synonyms (Soft appearance).
    * Explanation (Soft appearance).
* Examples, synonyms, and explanations must have an animation when switching (Flipping animation).
* The left and right arrow buttons must have feedback and click animations (feedback: button fill; animation: button tremor).

### Caching
* Previously translated text must be stored locally.
* Translation of text that has already been translated should happen instantly.
* The translation should be stored locally in full (all provided information).

### Errors
* If no translation language is selected — a message is shown.
* If the text is empty — the translation is not performed.
* If the Input language and output language match – only one flag with one language is displayed.
