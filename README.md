# Discord Casino Bot Development Plan

## Key Features to Implement

### 1. Main Menu
- Display the number of credits in the top-right corner:
  - Start with 6 credits per user weekly.
  - Link credits to Discord accounts to ensure persistence across sessions.
- Admin Mode:
  - Allow users with the "admin" role to add or remove credits from any account.

### 2. Games
#### A. 1v1 Games
1. **Craps Dice Game**:
   - Description: "Shoot dice versus other people to win 2x your bet!"
   - Betting Options: 5.20, 10.20, 20.20 credits.
   - Features:
     - Match players and provide a 20-second tutorial.
     - Calculate outcomes:
       - Winner: `(Bet x 2) - 0.4` credits.
       - Loser: Bet subtracted from balance.
     - Display results:
       - Winner: "You’ve won X credits!"
       - Loser: "You lost!"
     - Add a "Continue" button to return to the main menu.

2. **Minigolf Game**:
   - Description: "Go head to head in minigolf to win 2x your bet!"
   - Betting Options: 5.20, 10.20, 20.20 credits.
   - Features:
     - Match players and provide a 20-second tutorial.
     - Play five rounds to determine the winner.
     - Calculate outcomes:
       - Winner: `(Bet x 2) - 0.4` credits.
       - Loser: Bet subtracted from balance.
     - Display results and include a "Continue" button.

#### B. 1vAI Games
1. **Slots**:
   - Description: "Match 3 and win 3x your bet!"
   - Win Probability: 20%.
   - Betting Options: 5.20, 10.20, 20.20 credits.
   - Features:
     - Provide a 20-second tutorial.
     - Display results:
       - Win: "You’ve won X credits!"
       - Lose: "You lost!"
     - Add buttons for "Play Again" and "Back."

2. **Roulette**:
   - Description: "Pick the right color and win up to 10x."
   - Betting Options: 5.20, 10.20, 20.20 credits.
   - Features:
     - Provide a 20-second tutorial.
     - Display results:
       - Win: "You’ve won X credits!"
       - Lose: "Tough luck!"
     - Add buttons for "Play Again" and "Back."

### 3. Credits Management
#### A. Buy Credits
- Non-Interactable Text:
  - "1 USD = 1 CREDIT."
  - "$2.95 Processing Fee on Credit Purchase, 10 Credit Purchase Minimum."
- Button:
  - "Click to Buy Credits": Opens [GiftCardGranny](https://www.giftcardgranny.com/visa-gift-cards/predesign/).
  - After clicking, display instructions for payment:
    - Send payment to `TUFFGAMING4601@GMAIL.COM`.
    - Include Discord username in the eGift message.
    - Credits deposited within 24 hours.
- Add a "Continue" button to return to the main menu.

#### B. Trade Credits
- Non-Interactable Text:
  - "1 CREDIT = 1 USD."
  - "10 Credit Withdrawal Minimum."
- Button:
  - "Click to Trade Credits": Opens a support ticket in the Discord server.
  - Display instructions in the ticket channel:
    - State the number of credits to trade.
    - Admins will process the request.

### 4. Terms of Service
- Placeholder: Not defined in the current scope.

---

## Development Steps

### 1. Plan and Design
- **UI Design**:
  - Sketch main menu and game interfaces.
  - Design navigation flow between menus and games.
- **Database Design**:
  - User data: Discord ID, credit balance, game history.
  - Admin logs: Record credit changes made by admins.

### 2. Development
- Use **Discord.py** (Python) [py-cord] for bot creation.
- Implement:
  - Main menu with interactive buttons.
  - Games with logic for matchmaking, tutorials, and results.
  - Credits management commands and admin tools.

### 3. Testing
- Test features:
  - Games: Match outcomes with expected results.
  - Credit persistence: Ensure balances remain consistent across sessions.
  - Admin tools: Validate permissions and credit adjustments.
- Handle edge cases:
  - Insufficient credits.
  - Multiple concurrent games.

### 4. Deployment and Maintenance
- Deploy the bot to a hosting platform (e.g., AWS, Heroku, or Replit).
- Monitor performance and user feedback.
- Provide bug fixes and updates as needed.

---

