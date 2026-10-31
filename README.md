# On your forehead!

A team guessing game for the classroom, or for any group. One player holds the phone to their forehead without looking at it, and their team describes the word on the screen without saying it. The phone's motion sensors detect whether the player got it right.

**Play it:** https://lorenagmad.github.io/En-la-frente/

It works for any subject or topic, and for social events too: you write your own list of words, or load it from a file or a Google Sheet.

## How to play

1. **Set up a game.** Give it a name, write the concepts (one per line) and choose the options. The concepts are shared out at random between the two teams, with no repeats.
2. **Add the players** and put each one in a team. Every team needs at least one player.
3. **Toss the coin** to decide which team starts.
4. **Play.** The player shown on screen puts the phone on their forehead, screen facing the team, held sideways. A teammate taps the screen to start the turn, and the team describes the concept until the player guesses it or the time runs out.
5. **See the result.** The final screen shows the winner, the score for each team and every concept played, with who played it and how long it took.

A game in progress is saved on the device, so you can leave it and continue later from the home screen.

## Game modes

| Mode | How a turn works | Scoring |
| --- | --- | --- |
| **One turn, one concept** | Each turn is a single concept with its own time limit (30 seconds to 2 minutes). | +1 for a correct guess, −1 for a miss. You choose whether a team that guesses right keeps playing or hands over to the other team; after a miss, the other team always plays. |
| **Time attack** | Each team gets a timed round to guess as many concepts as it can, then the other team plays. You choose 1 to 5 rounds per team. | +1 for each correct guess. Passing a concept can cost nothing or 1 point. |

You can also limit how many concepts each team gets (5, 8, 10, 15, 20 or all of them).

## Phone movement

| Mode | Correct | Missed or pass |
| --- | --- | --- |
| One turn, one concept | Put the phone face down on the table | Put the phone face up on the table |
| Time attack | Tilt the phone down | Tilt the phone up |

Use **Test the movement** on the setup screen before playing. On iPhone, the browser asks for permission to use the motion sensors when you toss the coin.

If a phone has no motion sensors, or they don't respond, the game shows **Correct** and **Missed** (or **Pass**) buttons during each turn. You can hide them in the setup.

The sensors only work when the game is opened from its own address over HTTPS, such as the GitHub Pages link above. They don't work inside previews or embedded frames.

## Loading the concepts

- **Type or paste** them into the list, one per line. Duplicates are removed.
- **Import a file:** text (`.txt`), CSV, or spreadsheets (`.xlsx`, `.xls`, `.ods`). The first column is used, and a header such as "Concepts", "Words" or "Terms" is skipped.
- **From a Google Sheet:** share the sheet as "Anyone with the link" and paste its address. The first column is used.
- **Use the example:** a ready-made list of 20 digital imaging concepts, to try the game quickly.

## Activity log (xAPI)

For classroom use, the game can keep an activity log in [xAPI](https://xapi.com/) format. It is off by default.

- **What it records:** the start and end of the game, and every concept played: who played it, which team, whether it was guessed, how long it took and the final score.
- **Identification:** the player's name is always asked for. The email and an ID number can each be "Don't ask", "Optional" or "Required".
- **Consent:** when the log is on, the game asks you to confirm that the players know their activity is being recorded before you can start.
- **Download:** the log is downloaded as a `.json` file from the final screen, ready to import into a Learning Record Store (LRS) or to analyse.

To use the game outside the classroom, ask only for the name and leave the log off.

## Privacy

Everything stays on the device. The settings, the players, the game in progress and the activity log are stored in the browser (`localStorage`) and are never sent to a server. The game only connects to the internet to:

- load its fonts from Google Fonts,
- load a spreadsheet library from cdnjs, only when you import an `.xlsx`, `.xls` or `.ods` file,
- read a Google Sheet, only when you load one.

## Accessibility

- Large text designed to be read from a distance.
- Buttons and form fields work with the keyboard and show a visible focus.
- If the device has "reduce motion" turned on, the animations and confetti are switched off.
- Light and dark modes follow the device's setting.

## Running it yourself

The whole game is a single file, `index.html`, with no build step and no dependencies to install.

- **Locally:** open `index.html` in a browser. The motion sensors need HTTPS, so for a full test on a phone, publish it first.
- **On GitHub Pages:** in the repository, go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save. The game will be at `https://<user>.github.io/<repository>/`.

## Credits

Created by [TELA UCA](https://lorenagmad.github.io/tela_uca/) (Technology Enhanced Learning for All), Department of Computer Engineering, Campus de Jerez, University of Cádiz.
