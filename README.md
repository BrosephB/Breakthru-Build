# Breakthru
## Game Demo Video (click the image below to watch on youtube)
<a href="https://youtu.be/sHPxUBMjbvw" target="\_blank">
   <img src="https://github.com/BrosephB/Breakthru-Build/blob/main/breakthrough%20social%20media.png" alt="Breakthru demo video on youtube">
</a>

## Play the game <a href="https://dr-apple-games.itch.io/breakthru-2d" target="_blank">here!</a>

## Game Overview
Breakthru is an arcade-style game that takes the idea of one dimensional player movement from Atari breakout.

Control the pink paddle to bounce the ball and destroy all the blue bricks on the screen as fast as you can to win the game in record time! 

## Controls

### Computer
* Right arrow - rotate clockwise
* Left arrow - rotate counterclockwise

### Mobile
* Touch Right side of screen - rotate clockwise
* Touch left side of screen - rotate counterclockwise

## Static Properties, Managing Scenes and UI

An unexpected challenge with creating this game was managing scene navigation. Initially, I had considered using separate scenes for each UI, but although that would be very organized, It would involve plenty of destroying and re-instantiating of GameObjects if a user wants to jump between UI screens.

I decided to use one scene for UI menus and one scene for core game-play. I also had a Game Manager GameObject in both scenes. Since I had a game over screen, victory screen, and a main menu screen all in one scene, I scripted my game manager GameObject to carry the game’s victory status across scenes and to instantly show the proper screen when the scene loads. Since this information needs to be carried across screens, I needed the property to stay intact even if my game manager GameObject instance is destroyed. Thus, I made use of something called static properties.

Static properties are so useful for data persistence that I also used static properties to keep track of the user’s current and high score. 
