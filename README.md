# NumberGuess-Haskell

Welcome to the Number Guessing Game in Haskell!

## Overview

NumberGuess-Haskell is a fun and interactive project that lets you test your guessing skills. This simple game challenges you to guess a randomly generated number within a specified range. The program provides helpful feedback, telling you whether your guess is higher or lower than the target number, all while keeping track of the number of attempts you've made.

## How to Play

Ready to play? Here's how you can get started:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/specdrake28/NumberGuess-Haskell.git
   ```

2. **Build the Haskell Program:**
   ```bash
   ghc Guess.hs
   ```

3. **Run the Game:**
   ```bash
   ./Guess
   ```

4. **Follow the On-Screen Instructions:**
   - The game will greet you with instructions and generate a random number between 1 and 16.
   - You'll be prompted to enter your guess.
   - Based on your guess, the program will provide feedback, letting you know if your guess is too high or too low.
   - Continue guessing until you correctly guess the number.
   - The program will display the number of attempts it took you to guess the correct number.

## Example Code

Here's a glimpse of the code that powers this exciting game:

```haskell
import System.Random 

loop n tries = do
    putStrLn "Please guess the number"
    l <- getLine
    let i = read l :: Int
    if i == n
    then putStrLn $ "You GUESSED it in " ++ show tries ++ " tries. Congratulations!!!!"
    else if i > n
         then do
             putStrLn "Too High"
             loop n (tries+1)
         else do
             putStrLn "Too Low"
             loop n (tries+1)

main = do
    putStrLn "In this game, you will have to guess a number generated by the computer between 1 and 16. Let's START!!!"
    g <- randomRIO (1,16)
    loop g 1
```

## License

This project is licensed under the MIT License. For more details, please see the [LICENSE](LICENSE) file.

Enjoy the game, and may the odds be ever in your favor!
```

Feel free to use this improved README for your GitHub project. It provides a more engaging and informative introduction to your game.
