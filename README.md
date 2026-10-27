# Second Life Studio app demo

Clickable prototype for the CC0006 group proposal (T052 Cluster D Group 29). It shows how the NTU clothes exchange could work: self-graded donations, QR drop-off tags, volunteer spot-checks, a credit system with a semester cap, and volunteer rewards.

All items, names and balances are sample data. Credit values are proposals for the pilot.

## Run it

Open `index.html` in a browser. No build step. It loads fonts and a QR library from CDNs, so it needs an internet connection.

To host it, turn on GitHub Pages under Settings > Pages, with the source set to the `main` branch and the root folder.

## Where the numbers live

The credit rules sit in the `CFG` object near the top of the script in `index.html`:

- Base credits by condition: like new 4, good 2, damaged 1
- Material factor: natural 1, blend 0.75, synthetic 0.5 (rounded up, minimum 1)
- Donation cap: 15 credits per semester
- Volunteer rate: 2 credits per hour, outside the cap
- 1 credit = S$1 at the North Spine exchange

## Tabs

Wallet, Donate, Exchange, Volunteer and Check. Donate a item, then open Check to confirm it and release the credits.
