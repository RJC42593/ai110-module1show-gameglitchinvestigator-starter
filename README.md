# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.

The Game Glitch Investigator is a number-guessing game where the player tries to guess a secret number within a limited number of attempts. The game provides hints indicating whether the next guess should be higher or lower.

- [ ] Detail which bugs you found.

The main bug I found was that the hint messages were reversed. When a guess was higher than the secret number, the game sometimes displayed the wrong direction or no hint at all. I also discovered that starting a new game did not fully reset all game state values.

- [ ] Explain what fixes you applied.

  - I refactored the `check_guess()` function by moving it from `app.py` into `logic_utils.py`.
  - I fixed the hint logic so guesses above the secret number display "Go LOWER!" and guesses below the secret number display "Go HIGHER!".
  - I updated `app.py` to import and use the refactored function.
  - I fixed the new game functionality so the game state resets correctly when a new game starts.
  - I added a pytest test case to verify that a guess higher than the secret number returns the correct outcome and hint.


## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

## Demo Walkthrough

1. User starts a new game.
2. The secret number is 50.
3. User enters a guess of 40.
4. Game returns "Too Low" and displays the hint "Go HIGHER!".
5. User enters a guess of 60.
6. Game returns "Too High" and displays the hint "Go LOWER!".
7. User enters a guess of 50.
8. Game returns "Win" and displays "Correct!".
9. The score updates and the game ends.
10. User clicks "New Game" to start another round.

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
PS C:\Users\Jake Clark\Desktop\Codepath AI110\Game Glitch Investigator\ai110-module1show-gameglitchinvestigator-starter> py -m pytest

============================== 4 passed in 0.14s ==============================
```


## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
