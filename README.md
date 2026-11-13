# Safe Cracker

A one-safe-per-group vault page for a Grade 2 story-problem review (Reveal Math Unit 4).

## Links for each group's computer

Open the site with `?group=1` through `?group=6` at the end, for example:

- `https://realmrteacherman.github.io/SafeCracker/?group=1`
- `https://realmrteacherman.github.io/SafeCracker/?group=6`

The plain site address shows a page where students pick their safe.

## How it works

- Students type their 5-digit vault code from their code sheet and press **Open**.
- A wrong code shakes the safe and says how many digits are right (not which ones).
  Add `&hint=off` to a link to hide that count.
- The right code swings the door open on the treasure and shows the final challenge.
- An open safe stays open on that computer, even after a refresh.
- To lock it again, click **Teacher: close this safe** at the bottom right, then click again to confirm.

## The code

The code (12847) is not written in the page. Each digit is stored as a short SHA-256
fingerprint of `vault-<position>-<digit>`. To change the code, ask Claude to update
`DIGIT_PRINTS` in `index.html`.
