# Safe Cracker

A one-safe-per-team vault page for a Grade 2 story-problem review (Reveal Math Unit 4).

## Two games, one link each

- **Safe Cracker** (higher-level groups): https://realmrteacherman.github.io/SafeCracker/
- **Fall Fair Safe** (whole group, leveled down with the Scoot story problems): https://realmrteacherman.github.io/SafeCracker/fair/

Each link opens a "Click your team" menu with Team 1 to Team 6. Each team clicks its
button to get its own safe. **Change team** (bottom left of a safe) goes back to the menu.
Once a team names its safe or opens it, the menu shows that on the same computer.
The two games keep their progress separately.

## How it works

- Students type their 5-digit vault code from their packet and press **Open**.
- A wrong code shakes the safe and says how many digits are right (not which ones).
  To hide that count on one computer, add `&hint=off` to the end of the address after the team
  opens its safe (for example `...?group=3&hint=off`).
- The right code swings the door open on the treasure and shows the final challenge.
- An open safe stays open on that computer, even after a refresh.
- To lock it again, click **Teacher: close this safe** at the bottom right, then click again to confirm.

## The codes

The codes are not written in the pages. Each digit is stored as a short SHA-256
fingerprint of `vault-<position>-<digit>`. To change a code, ask Claude to update
`DIGIT_PRINTS` in that game's `index.html`.
