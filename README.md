# Voxel Technical Interview - SnakesAndLadders

Thanks for willing to apply to work with us. You can see our open positions [here](https://www.voxelgroup.net/people/en/home-eng/#page6)

We'd like you to solve this little coding exercise. It shouldn't take you more than one hour. The goal of the exercise is to get a glimpse of you as a developer and to be a starting point to have a conversation. 

## Exercise

Snakes and Ladders is a board game involving two or more players rolling dice in order to move their tokens across a board. The board is made up of a collection of numbered squares and is adorned with 'snakes' and 'ladders', which link two squares on the board- snakes link the squares downwards whilst ladders link them going upwards. This means that landing at the bottom of a ladder moves you to the top of that ladder, whereas landing on the top of a snake moves you to the bottom of that snake. The objective of the game is to get your token to the final square before your opponents do.

From a technical point of view, the implementation of this game needs to be platform agnostic. We are going to want to launch this game on multiple devices and need a solid, robust game library which we can use as the backend for every frontend we stick on it. For this reason, we are not interested in the frontend you choose to use to test the game, only that the core game logic is separate and tested. 

![board](/img/snakesandladdersboard.jpg)

The first feature we want implemented is the ability to move your token across the board using dice rolls. Players will need the ability to roll a dice, move their token the number of squares indicated by the dice roll and should win if they land on the final square. The feature is splitted in three user stories.

### US 1 - Token Can Move Across the Board
    As a player
    I want to be able to move my token
    So that I can get closer to the goal

**UAT1**

    Given the game is started
    When the token is placed on the board
    Then the token is on square 1
    
**UAT2**

    Given the token is on square 1
    When the token is moved 3 spaces
    Then the token is on square 4
    
**UAT3**

    Given the token is on square 1
    When the token is moved 3 spaces
    And then it is moved 4 spaces
    Then the token is on square 8
    
### US 2 - Player Can Win the Game
    As a player
    I want to be able to win the game
    So that I can gloat to everyone around
    
**UAT1**

    Given the token is on square 97
    When the token is moved 3 spaces
    Then the token is on square 100
    And the player has won the game
    
**UAT2**

    Given the token is on square 97
    When the token is moved 4 spaces
    Then the token is on square 97
    And the player has not won the game
    
### US 3 - Moves Are Determined By Dice Rolls

    As a player
    I want to move my token based on the roll of a die
    So that there is an element of chance in the game

**UAT1**

    Given the game is started
    When the player rolls a die
    Then the result should be between 1-6 inclusive
    
**UAT2**

    Given the player rolls a 4
    When they move their token
    Then the token should move 4 spaces
    
## General Requirements

- Application must use the console for input and output.
- Use an object oriented languaje, preferably C#. (provide instructions on how to run the application).
- Implement the requirements focusing on writing the best code you can produce.

## Evaluation
- Produce code that is readable and maintainable, object oriented design principles.
- UATs should be backed up by test.

## Code submission

- Add the code to your own Github account and send us the link.

Thanks and good luck!!
