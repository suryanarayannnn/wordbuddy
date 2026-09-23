# WordBuddy: a voice vocabulary tutor

A free voice tutor for English vocabulary that runs in your browser. It speaks one word at a time, quizzes you out loud, gives hints, and reviews words you've already learned.

**No account, no install, no data leaves your browser.**

## How to use it
1. Open the site in **Chrome or Edge** (desktop or Android) and press **Start lesson**.
2. Allow microphone access when the browser asks.
3. Answer out loud (tap the mic, or leave **Hands-free** on) or type your answer.

Things you can say at any time: `slower`, `faster`, `repeat`, `spell it`, `skip`, `easier`, `harder`, `what does <word> mean`.

## How it works
| Part | Technology |
|------|------------|
| Ears | Web Speech API speech recognition (Chrome/Edge) |
| Brain | A built-in tutor with 30 words across Beginner, Intermediate and Advanced levels |
| Voice | Web Speech API speech synthesis (every modern browser) |

The whole app is one file, `index.html`. Your progress is saved in your own browser only.

## Adding words
Open `index.html`, find `const BANK`, and add an entry to any level:

```js
{term:"eloquent", pos:"adjective", hint:"EL-uh-kwent",
 meaning:"able to speak or write clearly and persuasively.",
 example:"Her eloquent speech moved the whole room.",
 syn:["articulate","expressive","fluent"],
 keys:["speak","clear","persuasive","well"]}
```

`syn` holds the synonyms accepted in the synonym quiz. `keys` holds the words that count as a correct answer when the learner explains the meaning.

## The AI agent prompt
The "How it works" section on the page shows the prompt for an AI-powered version of this tutor. It works with Claude or any voice-agent platform.

## Known limits
- Voice input needs Chrome or Edge. Firefox and Safari fall back to typing, but the tutor still speaks.
- The microphone works only on `https://` pages (GitHub Pages is HTTPS) or `localhost`.

