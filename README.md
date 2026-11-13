# Safe Cracker

A one-safe-per-team vault page for a Grade 2 story-problem review (Reveal Math Unit 4).

## One link for every computer

https://realmrteacherman.github.io/SafeCracker/

The link opens a "Click your team" menu with Team 1 to Team 6. Each team clicks its
button to get its own safe. **Change team** (bottom left of a safe) goes back to the menu.
Once a team names its safe or opens it, the menu shows that on the same computer.

## How it works

- Students type their 5-digit vault code from their code sheet and press **Open**.
- A wrong code shakes the safe and says how many digits are right (not which ones).
  Add `?hint=off` to the link (or `&hint=off` after a team) to hide that count.
- The right code swings the door open on the treasure and shows the final challenge.
- An open safe stays open on that computer, even after a refresh.
- To lock it again, click **Teacher: close this safe** at the bottom right, then click again to confirm.

## The code

The code (12847) is not written in the page. Each digit is stored as a short SHA-256
fingerprint of `vault-<position>-<digit>`. To change the code, ask Claude to update
`DIGIT_PRINTS` in `index.html`.
