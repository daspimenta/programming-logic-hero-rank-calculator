# Hero Rank Calculator

![JavaScript](https://img.shields.io/badge/language-JavaScript-informational)
![License](https://img.shields.io/badge/license-MIT-blue)

A small JavaScript program that calculates a hero's net wins (wins minus defeats), assigns a rank based on the result, and prints a summary using the hero's first name.

## Table of Contents

- [How It Works](#how-it-works)
- [Rank Table](#rank-table)
- [Getting Started](#getting-started)
- [Example Output](#example-output)
- [Known Limitations](#known-limitations)
- [Roadmap](#roadmap)
- [License](#license)

## How It Works

1. `calculateNetWins(wins, defeats)` returns the difference between wins and defeats.
2. A `switch(true)` statement maps the net wins to a rank.
3. `getFirstName(name)` extracts the first word of the hero's full name.
4. The result is printed to the console.

## Rank Table

| Net wins     | Rank         |
|:-------------|:-------------|
| Below 0      | Invalid rank |
| 0 – 10       | Bronze       |
| 11 – 20      | Iron         |
| 21 – 50      | Silver       |
| 51 – 80      | Gold         |
| 81 – 90      | Diamond      |
| 91 – 100     | Legendary    |
| 101 and up   | Immortal     |

## Getting Started

### Prerequisites

A JavaScript runtime such as [Node.js](https://nodejs.org/), or a browser developer console.

### Installation

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### Usage

1. Open `index.js` and set the values at the top of the file:

   ```js
   let heroName = "Britney Vanilla Haddaway Spears";
   let wins = 300;
   let defeats = 200;
   ```

2. Run the program:

   ```bash
   node index.js
   ```

## Example Output

```text
Hero named Britney has 100 net wins and is at the Legendary level!
```

## Known Limitations

- A hero with more defeats than wins (negative net wins) is ranked as "Invalid rank".
- Decimal values for wins or defeats can fall between the defined ranges, so no rank is assigned.
- Inputs are not validated, so non-numeric values produce unexpected results.

## Roadmap

- [ ] Move the rank logic into its own function
- [ ] Validate the inputs
- [ ] Accept the hero's name, wins, and defeats as user input

## License

Distributed under the MIT License.
