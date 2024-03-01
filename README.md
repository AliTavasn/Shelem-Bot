# Shelem Bot
#### Video Demo:  <https://youtu.be/iFPp3YGVtvo>
## Description:
    Introduction
My name is Ali Tavassolinia and this is my final CS50P project.The project that I have prepared for this course is to create a Telegram bot that can be used to play Shelem and I used pyTelegramBotAPI(4.16.1) package to develop this robot. Shalem game is a 4 player game with Cards. if you want to know about this game rulles visit this link: https://en.wikipedia.org/wiki/Shelem#:~:text=Rules,-Card%2Dpoint%20values&text=Each%20player%20receives%2012%20cards,the%20widow%20and%20making%20trumps.

    Robot game process
First, to start the game, you have to type the robot's ID in any group or chat you want, and then the robot will show you the option to play the game through an Inline Query. When you click on this option, the first message of the robot will be sent in the group or chat (no need to add the robot in the group).

The bot then asks players to join the game and a "I am in" button is displayed below the message. Anyone who clicks this button will enter the list of players and their ID, username and first name will be saved in the robot. When the number of players reaches 4, the game starts automatically and the robot enters the next stage.

Now the robot divides the players into 2 groups and announces the grouping to them. Meanwhile, a number of buttons are displayed, which display numbers from 100 to 165 in 5 steps. That is, 100, 105, 110 and... . There is also a "pass" button below them for anyone who couldn't read a higher score press pass. If 3 players passed, the fourth player is determined as the ruler, Or if a player registers 165 points, he will rule. In any case, if any of these 2 situations happen, the ruler will be determined and the robot will display the next message.

When the ruler is selected, 4 cards are added to his cards, and at this stage the ruler must see his hand by clicking on the "My Hand" button and discard 4 cards. At this moment, the ruler has 16 cards, and each card is assigned a number from 1 to 16 respectively, and 16 buttons from number 1 to 16 are displayed. If the ruler wants to discard any card, he must press the desired button to remove that card from his hand. For example, the card number 8♠️ is 3, and by pressing on the 3 button, the card 8♠️ is deleted. When the ruler removes 4 cards, we enter the next stage, which is the main stage, and the whole game takes place here.

At this stage, the ruler starts first and throws his first card. The first card that the ruler throws is chosen as the ruling of the game. Then other players throw this card if they have it and if they don't have any other card they want. Then any player who takes this hand starts the next hand first and whatever card they throw, the others must throw a card with the same sign as that card if they have it. If the card does not have a mark, they throw another card. If they have a card and they want to throw another card, the robot prevents this and by sending a notification to their Telegram, it tells them that they should choose another card. Card selection in this stage is done like the previous stage with the numbers assigned to each card and this time, the numbers are between 1 and 12 because each player initially has 12 cards. Each time the hand ends, one card is subtracted from their cards and one button is also subtracted from the available buttons, and this process continues until all players discard all their cards and their hand is finished.

Now we have reached the final stage of the game, i.e. calculating the points and determining the winner. If the ruling group has obtained a score equal to or more than the score that the ruler read at the beginning, he wins the game, otherwise the other group is closed and the robot determines the winner after announcing the points. Below this message, there are two buttons, one is the "🔄️rematch", which by pressing this button, the game of Shalam is sent in the same chat or group, and the other button is "👥with friends", which by pressing it, a list of Telegram groups and chats is sent to someone who By pressing the button, it will be displayed that by selecting any of these chats, the Shalam game will be sent to that chat. And this process repeats itself.

This was a summary of my final project. I hope you enjoyed.
