# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

So for the first time I ran the game, it asked me to guess the mystery number while giving me 7 attempts to guess the right number with a clue. The range was 1 to 100, and everytime I guessed from 1-50 it said to go lower with the same hint. This should have logically triggered "go higher". When the round ended, the actual number was -35, which is well outside of range. The hint is also 63, which is unhelpful at all. The game also doens't reset properly between rounds, as the new game button doesn't work. The submit button for a number guess also doesn't always work?

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| Guess of 50 (secret was -35) | "Too Low" hint, since 50 > -35 | "Go lower" hint shown | none |
| Guess of 1 (secret was -35) | "Too High" or "Correct" hint, since 1 > -35 | "Go lower" hint still shown | none |
| Started a new game | New secret number between 1-100, input/history cleared | Secret was -35 (out of range), "63" shown as leftover secret, old guess history still visible | none |

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
