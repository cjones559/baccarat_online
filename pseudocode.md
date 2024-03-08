### Brainstorming 
---
[Baccarat](https://en.wikipedia.org/wiki/Baccarat) or Blackjack? 

* Single-player Baccarat is just more inventive, so lets go with that :>
* ## Baccarat Project
	*  If opening website, set an initialization function on onset to;
		* Set card table and playing surface as background;
		* Set a money counter on the top of the screen for continuous playing;
		* Set a large-enough amount for money counter to facilitate playing;
		* Set chip icons of value 100, 50, 25, 10, and 1 on the bottom of the screen;
		* Set play again button on the bottom-right of the screen to allow for continuous playthrough;
		* Set an initialize button on that calls the initialize function to the right of the play-again button, which has the difference of resetting the money counter to the initial amount;
	
	* Set program to take browser size into account: if browser window is less than 400 pixels wide, do not enable the game to be playable (this is necessary for ensuring proper spacing and appearance of game);
	
	* If the money counter hits zero, set a GAME OVER overlay to appear over top of the playing surface and have a 'bank!' button pop up to enable playing again;
		* this 'bank!' button will have the function of adding a set amount of money on click in the money counter and dismissing the GAME OVER overlay and 'bank!' buttons to facilitate playing;
		* otherwise proceed through the program structure; 

	* Enable player to input a bet amount on onset to three clickable sections: the banker, the player, or tie;

	* If chips are selected at the bottom of the screen, set chip amount into array and use to note running total of bets in lower right; 

	* If chips are set and player is ready, have the player click on a 'deal' button in the upper middle of the screen; all game logic proceeds as such:
		* Bet amount is stored in array, ready to be subtracted or added based on game results;
		* Cards drawn must be randomized from 2-10, ace, king, queen, jack;
		* 2-9 cards are worth face value, 10, king, queen, and jack are worth 0, and aces are low(1);
		* For the game to work, the last number of the sum of the cards drawn is the actual hand value; select the last digit of the player hand and compare that value to the dealer's hand's last digit;
		* If player has a 'natural win'(player hand is larger than dealer hand at outset), play again button appears and bet amount is paid out or withdrawn (based on the player's bets); 
			* otherwise, a third card is drawn for the player hand (only for 0-5 hands) or banker hand (if hand is worth 0-2), with the dealer drawing a second card based on the proceeding logic;
				* The third card is always drawn sideways, which is a pre-set choice and will always occur as such;
				*  If the Player’s third card is 9, 10, face-card or Ace, the Banker draws when he has a 0-3, and stays with a 4-7;
				- If the Player’s third card is 8, the Banker draws when he has a 0-2, and stays with a 3-7.
				- If the Player’s third card is 6 or 7, the Banker draws when he has a 0-6, and stays with a 7.
				- If the Player’s third card is 4 or 5, the Banker draws when he has a 0-5, and stays with a 6-7.
				- If the Player’s third card is 2 or 3, the Banker draws when he has a 0-4, and stays with a 5-7.
		* If player and banker draw 6 on opening hand, it's a draw;
		* If player AND banker opening two cards are 8 or 9, then no other cards are drawn and the game ends on that hand;
		* The winner is selected by which hand is closer to 9; payout bets for the player;
		*  Payout for banker and player are 1:1, however if the player bets on the banker, bets take .05 of the winnings as commission; 
		* Payout for ties are 8:1 or 9:1 (I'll choose 8:1 cuz I'm stingy); 
		* If player selects bets that are not fulfilled, subtract bet amount from money counter;

	* If player has some integer amount within money counter, repeat game from 'Enable player to input a bet amount';
--- 

