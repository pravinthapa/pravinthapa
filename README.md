# 🧩 Try My Mini Puzzle

> **Hint:** Copy the code below into your browser console and see if you can solve it!  
> The puzzle will reveal a hidden message if you get it right.

```javascript
(function() {
  const answer = "PRABIN";
  let tries = 3;

  console.log("%cWelcome to Prabin's Puzzle! 🧩", "color: #4ade80; font-size: 18px; font-weight: bold;");
  console.log("Guess my name in ALL CAPS. You have 3 tries.");

  window.guessName = function(name) {
    if (name.toUpperCase() === answer) {
      console.log("%c🎉 Correct! Welcome to my GitHub profile.", "color: #3b82f6; font-size: 16px; font-weight: bold;");
    } else {
      tries--;
      if (tries > 0) {
        console.log(`❌ Wrong! You have ${tries} tries left.`);
      } else {
        console.log("💀 Game over! Refresh to try again.");
      }
    }
  };

  console.log("Type %cguessName('YOUR_GUESS')%c in the console to play.", "color: #facc15", "");
})();
