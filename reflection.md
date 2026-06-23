# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?

When I first ran the game, it looked like a normal number-guessing game with difficulty settings, hints, and a developer debug panel. However, after playing a few rounds, I noticed several inconsistencies between what the game displayed and how it actually behaved. One bug was that pressing Enter did not submit a guess, forcing me to click the Submit button every time. Another bug was that the hint system sometimes gave impossible instructions, such as telling me to guess higher after I entered 100, even though 100 is the maximum allowed value. I also noticed that the attempts displayed in the sidebar did not always match the attempts shown in the developer debug information.
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|--------|-------------------|-----------------|------------------------|
| Guess = 100 when secret was 39 | Game should indicate the guess is too high or out of range | Hint displayed "GO HIGHER!" even though 100 is the maximum value | None |
| Press Enter after typing a guess | Guess should be submitted | Nothing happened; had to click Submit Guess | None |
| Secret number shown as 58 in Debug Info and guess entered as 58 | Game should immediately register a win | Game did not correctly recognize the winning guess | None |
| Hard difficulty selected | Attempts and range should be consistent everywhere | Sidebar attempts and debug attempts did not always match | None |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
