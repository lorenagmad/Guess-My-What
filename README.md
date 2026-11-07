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
- **Download:** the log is downloaded as a `.json` file from the final screen, ready to open in the [analysis panel](#analysis-panel) or to import into a Learning Record Store (LRS).
- **Format:** the field names and response values are the same in both languages, so logs from Spanish and English games can be analysed together. The verb and activity names are written in the game's language and tagged with it (`es-ES` or `en-US`).

To use the game outside the classroom, ask only for the name and leave the log off.

## Analysis panel

The analysis panel turns the activity logs into a summary of how your class played: which concepts were hardest, how each game went and how each player did. It is a separate page that runs entirely in your browser: the files you load are **not uploaded anywhere**.

**Open it:** https://lorenagmad.github.io/Guess-My-What/panel.html

The panel is in Spanish for now. It reads logs from games played in either language.

### Step by step

1. **Before playing, turn on the log.** On the setup screen, set **Activity log (xAPI)** to **Keep a log**. Choose whether to ask for the email and the ID number (*Don't ask* is enough for the panel; the player's name or a nickname is always asked for).
2. **Play the game** as usual.
3. **Download the log** from the final screen with **Download the log (xAPI)**. Do it before you start another game: the log is kept on the device only until then. You get a file called `guess-my-what_….json`.
4. **Open the panel** and drag the files onto the dashed box, or press **Elegir archivos** (*Choose files*). You can load several files at once, from different groups and days: they are merged and duplicates are removed.
5. **Read the results.** Use the filters at the top to see one game (or subject) or one mode.
6. **Export** what you need as CSV files, which open in Excel or LibreOffice.

To start again with other files, press **Vaciar** (*Clear*).

### What you see

| Section | What it shows |
| --- | --- |
| Summary | Number of games, players and concepts played, percentage guessed, median time to guess and how many concepts were missed at least once. |
| **Repaso** (*Review*) | The concepts that cost the most, with their definition and forbidden words, ready to go over in class. You can download it as CSV or copy it. |
| **Tres rondas** (*Three rounds*) | Only for *Three rounds* games: how the success rate changes from describing freely, to one word, to mime. |
| **Conceptos** (*Concepts*) | Each concept: times played, guessed, missed, passed and median time. Click a column to sort. |
| **Partidas** (*Games*) | Each game: date, name, mode, final score, concepts played, success rate and duration. |
| **Jugadores** (*Players*) | Each player: team, concepts played with the phone on their forehead, success rate and median time. |

### Hiding personal data

The **Ocultar datos identificativos** (*Hide identifying data*) box at the top is **ticked by default**. While it is ticked, names, emails and ID numbers are replaced by codes (J-01, J-02…) on screen and in every export, and the names of the loaded files are hidden. Untick it only if you need to see who is who, for example to give feedback to a student.

Keep in mind:

- The codes are assigned each time you load files, in alphabetical order of the players. If you load a different set of files, the same person may get a different code.
- Hiding only affects the panel. **The `.json` files you downloaded still contain whatever the players typed** (name or nickname and, if you asked for them, email and ID number). Store them as you would any other student data, for example on your institution's storage, and delete them when you no longer need them.
- To collect as little personal data as possible, ask players to use a nickname or a code instead of their real name, and set the email and the ID number to *Don't ask*.
- If you use the data for research, you need the participants' informed consent and the approval your institution requires. Publish only aggregated results.

## Privacy

Everything stays on the device. The settings, the players, the game in progress and the activity log are stored in the browser (`localStorage`) and are never sent to a server. The analysis panel reads the files you load in your browser and does not send them anywhere either. The game and the panel only connect to the internet to:

- load their typefaces from Google Fonts (no game data is sent),
- read a Google Sheet, only when you load one.

## Design and accessibility

- Colours from the [TELA UCA](https://lorenagmad.github.io/tela_uca/) logo and a single typeface, Nunito, chosen to be read from a distance.
- Buttons and form fields work with the keyboard and show a visible focus.
- If the device has "reduce motion" turned on, the animations and confetti are switched off.
- Light and dark modes follow the device's setting.

## Running it yourself

The whole game is a single file, `index.html`, and the analysis panel is another, `panel.html`. There is no build step and no dependencies to install.

- **Locally:** open `index.html` in a browser. The motion sensors need HTTPS, so for a full test on a phone, publish it first.
- **On GitHub Pages:** in the repository, go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save. The game will be at `https://<user>.github.io/<repository>/` and the panel at `https://<user>.github.io/<repository>/panel.html`.

## Authors

- Lorena Gutiérrez Madroñal
- Rubén Baena Pérez
- José Miguel Mota Macías
Department of Computer Engineering, Campus de Jerez, University of Cádiz.

![License: AGPL-3.0-or-later](https://img.shields.io/badge/license-AGPL--3.0--or--later-blue)
