# Random Number Guessing Game Flowchart

This flowchart represents the sequence of events necessary for a computer program to implement a random number guessing game. The program follows these steps:

1. **Start the Game**: The program starts.
2. **Generate Random Number**: The program generates a random number within a specific range (e.g., 1 to 100).
3. **User Input**: The user guesses the number.
4. **Validation**: The program checks if the input is correct (e.g., number, within range).
5. **Feedback**: The program provides feedback based on the guess:
   - Too high
   - Too low
   - Correct

6. **Repeat or End**: If the guess is incorrect, the program repeats the process. If correct, it ends the game.

---

```mermaid
flowchart TD
    A[Start the Game] --> B[Generate Random Number]
    B --> C[User Guesses a Number]
    C --> D{Is the Number Correct?}
    D -->|No| E[Error Appears: Incorrect Number]
    E --> C
    D -->|Yes| F{Is the Guess Correct?}
    F -->|Too Low| G[Feedback: Guess Too Low]
    F -->|Too High| H[Feedback: Guess Too High]
    F -->|Correct| I[Feedback: Correct! ]
    G --> C
    H --> C
    I --> J[End Game]
