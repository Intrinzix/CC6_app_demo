# Second Life Studio app demo

Clickable prototype for the CC0006 group proposal (T052 Cluster D Group 29). It shows how the NTU clothes exchange could work: self-graded donations, QR drop-off tags, volunteer checks, a credit system with a semester cap, a 30-day shelf clock and volunteer rewards.

All items, names and balances are sample data. Credit values are proposals for the pilot.

## Run it

Open `index.html` in a browser. No build step. It loads fonts and a QR library from CDNs, so it needs an internet connection.

Live version: https://intrinzix.github.io/CC6_app_demo/ (GitHub Pages, `main` branch, root folder).

## Two views

The switch at the top of the phone changes the role.

- **Student:** Wallet, Donate, Exchange, Shifts.
- **Volunteer desk:** Scan (check incoming tags), Stock (shelf countdown and bin counts).

Try this path: in Student view, go to Donate and get a tag. Switch to Volunteer desk, open Scan, and confirm the tag. Switch back to Student and the credits are in the Wallet, with the item on the Exchange shelf.

## Where the numbers live

The credit rules sit in the `CFG` object near the top of the script in `index.html`:

- Base credits by condition: like new 4, good 2, damaged 1
- Material factor: natural 1, blend 0.75, synthetic 0.5 (rounded up, minimum 1)
- The same table sets what an item earns when donated and what it costs on the shelf
- Donation cap: 15 credits per semester
- Volunteer rate: 2 credits per hour, outside the cap
- Shelf time: 30 days, then the item goes to a partner
- 1 credit = S$1 at the booth
