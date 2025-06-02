# Hangman Game 🎮

A classic word-guessing game implemented in Python where players try to guess a hidden word letter by letter before running out of lives.

## 📝 Description

This Hangman game challenges players to guess a randomly selected word from a predefined list. Players have 6 lives to guess the word correctly. Each incorrect guess results in losing a life and progressing through ASCII art stages of a hangman drawing. The game ends when either the word is completely guessed (win) or all lives are lost (lose).

## 🎯 Features

- Random word selection from a fruit-themed word list
- Interactive letter-by-letter guessing
- Visual hangman ASCII art progression
- Life counter system (6 lives total)
- Win/lose game states with appropriate messages
- Real-time display of guessed letters in their correct positions

## 🔧 How It Works

### Game Flow
1. **Initialization**: The program randomly selects a word from the predefined list
2. **Display Setup**: Creates a list of underscores representing each letter in the word
3. **Game Loop**: Continues until win or lose condition is met
4. **Input Processing**: Takes user's letter guess and checks against the target word
5. **State Updates**: Updates display, life counter, and hangman visual
6. **End Game**: Declares winner or game over based on conditions

### Core Components

#### Word Selection
```python
l1=["apple","banana","guvava","grapes"]
computer_choice=random.choice(l1)
```
- Uses Python's `random.choice()` to select from predefined fruit words
- Words include: apple, banana, guava, grapes

#### Display System
```python
l2=[]
for i in range(len(computer_choice)):
    l2.append("_")
```
- Creates placeholder underscores for each letter in the selected word
- Updates with correctly guessed letters in their proper positions

#### Life Management
- Starts with 6 lives
- Decrements by 1 for each incorrect guess
- Game ends when lives reach 0

#### Visual Feedback
- ASCII art hangman drawings showing game progression
- 7 stages from empty gallows to complete hangman figure
- Corresponds to remaining lives (6 down to 0)

## 🚀 Getting Started

### Prerequisites
- Python 3.x installed on your system
- No additional libraries required (uses built-in `random` module)

### Installation & Running
1. Clone this repository or download the Python file
2. Navigate to the project directory
3. Run the game:
```bash
python hangman.py
```

### How to Play
1. The game will display underscores representing the hidden word
2. Enter one letter at a time when prompted
3. Correct guesses reveal the letter's position(s) in the word
4. Incorrect guesses reduce your remaining lives
5. Win by guessing all letters before running out of lives
6. Lose if the hangman drawing is completed (0 lives remaining)

## 📊 Game States

### Winning Condition
- All letters in the word have been correctly guessed
- Displays: "you won the game with remaining life [X]"

### Losing Condition  
- All 6 lives have been used up
- Displays: "game over you loose the game"

### Live Feedback
- Current word state with guessed letters filled in
- Remaining lives counter
- Current hangman ASCII art stage

## 🎨 ASCII Art Stages

The game features 7 distinct hangman drawing stages:
- Stage 6: Empty gallows
- Stage 5: Head appears
- Stage 4: Body added
- Stage 3: Left arm added
- Stage 2: Right arm added  
- Stage 1: Left leg added
- Stage 0: Complete hangman (game over)

## 🔄 Game Logic Flow

```
START → Select Random Word → Initialize Display → 
Get User Input → Check Letter → Update Display/Lives → 
Check Win/Lose Conditions → Continue/End Game
```

## 🛠️ Technical Implementation

### Data Structures
- **List**: Used for word bank, display state, and ASCII art stages
- **String**: Stores the target word and user input
- **Boolean**: Controls game loop and end states
- **Integer**: Tracks remaining lives

### Control Flow
- **While Loop**: Main game loop controlled by `game_over` boolean
- **For Loop**: Iterates through word characters for comparison
- **Conditional Statements**: Handle game logic and state changes

### Key Functions Used
- `random.choice()`: Random word selection
- `input()`: User interaction
- `print()`: Display output
- `len()`: String/list length calculation
- `range()`: Loop iteration
- `append()`: List manipulation

## 🎮 Example Gameplay

```
['_', '_', '_', '_', '_']
try to guess the letter in word: a
['a', '_', '_', '_', '_']
5
[Hangman Stage 5 ASCII Art]

try to guess the letter in word: p
['a', 'p', 'p', '_', '_']
5
[Hangman Stage 5 ASCII Art]

try to guess the letter in word: l  
['a', 'p', 'p', 'l', '_']
5
[Hangman Stage 5 ASCII Art]

try to guess the letter in word: e
['a', 'p', 'p', 'l', 'e']
you won the game with remaining life 5
```

## 🚧 Future Enhancements

- Add difficulty levels with different word categories
- Implement hint system
- Add scoring based on remaining lives
- Include word definitions after game completion
- Save high scores and game statistics
- Add multiplayer functionality
- Expand word database with external file input
- Implement GUI version using tkinter or pygame

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements. Some areas for contribution:
- Bug fixes and code optimization
- Additional word categories
- Enhanced ASCII art
- Better user interface
- Code documentation improvements

## 📄 License

This project is open source and available under the MIT License.

---

*Enjoy playing Hangman! Challenge yourself to guess the words with as few wrong guesses as possible.* 🎯
