# Shiritori Word Game

A real-time multiplayer word chain game based on the Japanese word game "Shiritori" built with Next.js and React.

![Shiritori Game](https://wanderingtanuki.com/wp-content/uploads/2021/12/title-2.png)

## What is Shiritori?

Shiritori (しりとり) is a Japanese word game in which players take turns saying words that begin with the last letter of the previous word. This digital version adds exciting features like time pressure, scoring based on word length, and a competitive two-player format.

## Features

- 🎮 Two-player turn-based gameplay
- ⏱️ Time pressure with countdown timer
- 🔤 Automatic validation of Shiritori rules
- 🎯 Score tracking with bonuses for longer words
- 📝 Word history tracking
- 🚫 Duplicate word detection
- 📱 Responsive design for desktop and mobile

## Tech Stack

- Next.js 14 (App Router)
- React 18
- Tailwind CSS
- shadcn/ui Components
- TypeScript

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/shiritori-game.git
cd shiritori-game
```

Install dependencies:

```bash
npm install
# or
yarn install
# or
pnpm install
```

Run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the app.

## Gameplay Instructions

### Basic Rules

1. The first player can enter any word to start the game
2. The next player must enter a word that begins with the last letter of the previous word
3. Words cannot be repeated
4. Players have 15 seconds to enter a valid word
5. If a player fails to enter a valid word within the time limit, their turn is skipped

### Scoring System

- Players earn points based on:
  - **Time remaining**: Up to 15 points (decreases by 1 each second)
  - **Word length bonus**: Words longer than 4 letters earn +1 point per additional letter
    - Example: "elephant" (8 letters) earns +4 bonus points (8-4=4)

### Example Round

1. Player 1 enters "apple"
2. Player 2 must enter a word starting with "e" (like "elephant")
3. Player 1 must then enter a word starting with "t" (like "table")
4. And so on...

## Project Structure

```bash
/shiritori-game
├── app/                  # Next.js App Router
├── components/           # React components
│   ├── ui/               # UI components from shadcn
│   └── PlayerCard.tsx    # Main game component
├── lib/                  # Utility functions
├── models/               # TypeScript type definitions
│   └── types.ts          # Game data types
├── public/               # Static assets
└── ...                   # Configuration files
```

## Customization

You can modify game parameters in the PlayerCard component:

- Time limit (default: 15 seconds)
- Word length bonus threshold (default: 4 characters)
- Number of players (current implementation: 2 players)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- [Next.js](https://nextjs.org/)
- [shadcn/ui](https://ui.shadcn.com/)
- [Tailwind CSS](https://tailwindcss.com/)
