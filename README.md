# Human Stress Test (Games App)
Game app created from Dart for users to play three mini games to test your human senses and reduce stress.

## About the App
Relieve your stress while playing games that test your reaction speed, memory, and physique. Our games are designed to be quick and fun, so try them out if you got 30 seconds!

## How to Build and Run Project
Run 'flutter pub get' in your terminal.

Memory Game consists of three views: one for the initial sequence to memorize, called MemoryGameView, one for actually playing the game and drawing the shapes, called MemoryGameQuetionView, and one to display the results, called MemoryGameResultView. There is a MemoryGame object that keeps track of the game data, like what shape of the sequence the user is currently on, and what shape they’re supposed to draw. There is also a MemoryGameProvider that tracks the user’s current index and when the game ends so it knows when to store the results.

One of the main views is the Stats page where it keeps track of the user’s data, it consists of each app’s best records and games played that are maintained and accessed through each game’s provider and stored in Hive’s secure storage. 

## Data Design and Data Flow 
We followed the general structure used in Journal App to have each game played as a record class and a list of records to keep track of all the user’s data. We did this with all the games we have and stored them using Hive’s secure storage. All of the changes are made and accessed through each game’s provider. We inserted a new record every time the provider’s ‘end game’ function is called. Each of our games has a provider (Memory Game has two, one for drawing and one for the game) which we used to update other elements of our app as the user performed actions.

## Authors and Acknowledgment
App created by Amy Cheng, Steven Tang, Benjamin So, Charyl Li, and Ramses Lee for a computer science course project.
