# Guess My What?!

[![DOI](https://zenodo.org/badge/1441040302.svg)](https://doi.org/10.5281/zenodo.24011643)

**English** · [Español](README.es.md)

A team guessing game for the classroom, or for any group. One player holds the phone to their forehead without looking at it, and their team describes the word on the screen without saying it. The phone's motion sensors detect whether the player got it right.

**Play it:** https://lorenagmad.github.io/Guess-My-What/

It works for any subject or topic, and for social events too: you write your own list of concepts, or load it from a Google Sheet.

## Languages

The game is in **English** and **Spanish**. Choose the language with the **Español / English** buttons at the top of the home screen. The first time, the game uses the device's language; after that, it remembers your choice.

Switching language also translates the default team names, the default game name and the example list. Names and concepts you have typed yourself are kept as they are.

## How to play

1. **Set up a game.** Give it a name, write the concepts and choose the mode and options.
2. **Add the players** and put each one in a team. Every team needs at least one player.
3. **Toss the coin** to decide which team starts.
4. **Play.** The player shown on screen puts the phone on their forehead, screen facing the team, held sideways. A teammate taps the screen to start, and the team describes the concept until the player guesses it or the time runs out.
5. **See the result.** The final screen shows the winner, each team's score and every concept played, with who played it and how long it took.

A game in progress is saved on the device, so you can leave it and continue later from the home screen.

## Modes

| Mode | How it works | Scoring |
| --- | --- | --- |
| **Turns** | Each turn is a single concept with its own time limit (30 seconds to 2 minutes). | +1 for a correct guess, −1 for a miss. You choose whether a team that guesses right keeps playing or hands over to the other team; after a miss, the other team always plays. |
| **Time attack** | Each team gets a timed round to guess as many concepts as it can, then the other team plays. You choose 1 to 5 rounds per team. | +1 for each correct guess. Passing a concept can cost nothing or 1 point. |
| **Three rounds** | The same concepts are played three times: **1.** describe them freely, **2.** with one word only, **3.** with mime only. Teams take timed turns; a passed concept goes back to the end of the pile. When a round's concepts run out, the next round starts. | +1 for each correct guess. Passing a concept can cost nothing or 1 point. |

You can also limit how many concepts are used (5, 8, 10, 15, 20 per team, or all of them).

## Concepts

Write one concept per line. Each line can also carry **forbidden words** and a **definition**, separated by asterisks:

```
Umbrella * rain, wet, open * Object you open to keep the rain off
```

- **Forbidden words** appear under the concept during the game, so the team knows what not to say. If someone says one, the concept counts as missed or is passed. You can hide them in the setup. In **Three rounds** they are shown only in the first round.
- **The definition** is saved with each concept in the activity log.
- Duplicates are removed. The counter under the list shows how many concepts have forbidden words or a definition.

Other ways to fill the list:

- **From a Google Sheet:** share the sheet as "Anyone with the link" and paste its address. Column A is the concept, column B the forbidden words (separated by commas) and column C the definition. A header such as "Concepts" is skipped.
- **Use the example:** 20 everyday concepts, with forbidden words and definitions, in the language you have chosen.
- **Clear the list:** removes every concept. Tap it twice to confirm.

## Phone movement

| Mode | Correct | Missed or pass |
| --- | --- | --- |
| Turns | Put the phone face down on the table | Put the phone face up on the table |
| Time attack and Three rounds | Tilt the phone down | Tilt the phone up |

Use **Test the movement** on the setup screen before playing. On iPhone, the browser asks for permission to use the motion sensors when you toss the coin.

If a phone has no motion sensors, or they don't respond, the game shows **Correct** and **Missed** (or **Pass**) buttons during each turn. You can hide them in the setup.

The sensors only work when the game is opened from its own address over HTTPS, such as the GitHub Pages link above. They don't work inside previews or embedded frames.

## Activity log (xAPI)

For classroom use, the game can keep an activity log in [xAPI](https://xapi.com/) format. It is off by default.

- **What it records:** the start of the game (mode, teams and their players, number of concepts, time limit, whether forbidden words are shown), every concept played (who, which team, whether it was guessed, how long it took, how it was marked: sensor, button or time, the round, and its forbidden words and definition) and the final score.
- **Identification:** the player's name is always asked for. The email and an ID number can each be "Don't ask", "Optional" or "Required".
- **Consent:** when the log is on, the game asks you to confirm that the players know their activity is being recorded before you can start.
- **Download:** the log is downloaded as a `.json` file from the final screen, ready to import into a Learning Record Store (LRS) or to analyse.
- **Format:** the field names and response values are the same in both languages, so logs from Spanish and English games can be analysed together. The verb and activity names are written in the game's language and tagged with it (`es-ES` or `en-US`).

To use the game outside the classroom, ask only for the name and leave the log off.

## Privacy

Everything stays on the device. The settings, the players, the game in progress and the activity log are stored in the browser (`localStorage`) and are never sent to a server. The game only connects to the internet to:

- load its typeface (Nunito) from Google Fonts,
- read a Google Sheet, only when you load one.

## Design and accessibility

- Colours from the [TELA UCA](https://lorenagmad.github.io/tela_uca/) logo and a single typeface, Nunito, chosen to be read from a distance.
- Buttons and form fields work with the keyboard and show a visible focus.
- If the device has "reduce motion" turned on, the animations and confetti are switched off.
- Light and dark modes follow the device's setting.

## Running it yourself

The whole game is a single file, `index.html`, with no build step and no dependencies to install.

- **Locally:** open `index.html` in a browser. The motion sensors need HTTPS, so for a full test on a phone, publish it first.
- **On GitHub Pages:** in the repository, go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save. The game will be at `https://<user>.github.io/<repository>/`.

## Authors

- Lorena Gutiérrez Madroñal
- Rubén Baena Pérez
- José Miguel Mota Macías
Department of Computer Engineering, Campus de Jerez, University of Cádiz.

![License: AGPL-3.0-or-later](https://img.shields.io/badge/license-AGPL--3.0--or--later-blue)
