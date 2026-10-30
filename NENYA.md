# Nenya (Durable Intelligence)

Nenya keeps AI agents on the rules and commitments the team sets: suppression list, consent, credit budget. Judges score whether we kept our rules and used Nenya.

## Install

Installed Oct 30, 2026: Nenya 1.0.3, for this Windows account (vladmaly7@gmail.com).

```
npx -y @qwntllabs/nenya setup     # install and open Nenya
npx -y @qwntllabs/nenya repair    # reinstall over the existing copy
```

Setup installs the Nenya app for the account; it adds no files to this repo.

## Commands

```
nenya setup               Install Nenya for this account and open it.
nenya repair              Install Nenya again over the copy that is there.
nenya message             Message a teammate in your swarm through Nenya (nenya message --help).
nenya tools               The tools Nenya learned in this repo: list, describe, run (nenya tools --help).

--invite CODE             Open Nenya with this invite code filled in.
--channel NAME            Release channel: alpha, beta or stable.
```

Run them as `npx -y @qwntllabs/nenya <command>` if `nenya` is not on the PATH.

## Our rules

To fill in once the team agrees them:

- Suppression list:
- Consent basis:
- Credit budget (Cargo / FullEnrich):
