# Secure Blockchain Voting System

Full website with:

- Register and login pages
- One-user-one-vote enforcement
- Blockchain-style vote ledger with linked hashes
- Final counting dashboard with live results
- Structured and responsive UI

## Run

1. Install dependencies:

```bash
npm install
```

2. Create environment file:

```bash
copy .env.example .env
```

3. Start server:

```bash
npm start
```

Open [http://localhost:3000](http://localhost:3000).

## Security Notes

- Passwords are hashed with `bcrypt` (`12` salt rounds).
- Authentication uses JWT bearer tokens.
- Vote endpoint requires auth and blocks duplicate voting per user.
- Each vote creates a mined block (simple proof-of-work prefix `000`) linked to the previous block hash.

## Tech Stack

- Backend: Node.js, Express, SQLite
- Frontend: HTML, CSS, Vanilla JavaScript
