# Security

## Reporting a problem

Please report a security problem privately, not in a public issue: use **Report a vulnerability** on the repository's Security tab (GitHub private vulnerability reporting). Say which Foundry, game system, and Path Keeper versions you used and how to reproduce it.

## What Path Keeper trusts

Path Keeper runs entirely inside Foundry. It makes no network requests of its own, loads no outside code, and creates no macros.

- **Players are not trusted.** A player's plans and requests live on that player's own Foundry user record, which only that player (and a GM) can change, so a request's sender is known. The GM's client rebuilds every new character from the installed compendiums and checks it against the GM's book and rarity settings; it does not take the player's word for what an item is.
- **Only GMs decide.** Creating a character, approving a plan, and applying retraining, a rebuild, or corrections run on a GM's client. A player applies the approved levels of a character they own, and can change only characters they own, as Foundry itself allows.
- **Whoever can change world settings is a GM to Path Keeper.** The request queue, approved plans, and GM configuration are world settings. Give Foundry's *Modify Configuration Settings* permission only to roles you trust as GMs.

## What other players can read

Foundry lets every user in a world read world settings and other users' flags. Saved plans, the request queue, and the notes a GM writes when sending a request back are therefore readable by the other players in the same world, with a browser console. Do not put anything private in a plan name or a send-back note.

## Supported versions

Fixes are made on the latest release.
