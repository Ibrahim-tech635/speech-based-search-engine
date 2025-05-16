# speech-based-search-engineaThe file **`speech based search engine (2).py`** is a Python script that uses voice input to perform a Google search. Here's a breakdown of what it does:

---

### 🔧 **Libraries Used**

* `speech_recognition`: Converts speech to text.
* `pyttsx3`: Text-to-speech engine.
* `webbrowser`: Opens URLs in the default browser.

---

### 📜 **Workflow Summary**

1. **Initialize Speech Engine:**

   ```python
   engine = pyttsx3.init()
   ```

2. **Text-to-Speech Function (`speak`)**
   Speaks out the given text:

   ```python
   def speak(text):
       engine.say(text)
       engine.runAndWait()
   ```

3. **Voice Command Input (`take_command`)**

   * Listens for user's voice.
   * Converts audio to text using Google's speech recognition API.
   * Handles errors if speech is not recognized or the API fails.

4. **Perform Web Search (`search_web`)**

   * Builds a Google search URL using the voice query.
   * Opens the search results in a web browser.
   * Speaks confirmation.

5. **Main Logic**

   * When the script runs, it listens for a voice command and then opens the corresponding Google search page:

   ```python
   if __name__ == "__main__":
       query = take_command()
       search_web(query)
   ```

---

### ▶️ **To Run This Script**

You’ll need:

* A working microphone.
* An internet connection (for Google Speech Recognition).
* The required Python libraries:

  ```bash
  pip install SpeechRecognition pyttsx3
  ```

---

