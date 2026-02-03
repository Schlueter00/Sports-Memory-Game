This README provides a comprehensive overview of the Sports Memory Game application, its features, and how to deploy it.

🏆 Sports Memory Game
A real-time, multiplayer memory matching game featuring all teams from the NFL, NBA, and MLB. Built with a focus on mobile responsiveness and seamless peer-to-peer connectivity, this game allows sports fans to compete across the hall or across the country without a central server.

✨ Key Features
Real-Time Multiplayer: Powered by PeerJS for serverless, low-latency peer-to-peer gameplay.

Comprehensive Rosters: Includes all 32 NFL teams, 30 NBA teams, and 30 MLB teams with high-quality SVG logos.

Host Controls:

Dynamic Grid Size: Choose between 16, 24, or 32 cards.

League Selection: Filter games by specific leagues or play a "Super Bowl" style mix of all three.

Leaderboard Management: Track "Season Wins" across multiple rounds and reset them at any time.

Room Management: Generate new Game IDs or reshuffle cards instantly.

Smart Game Logic: * Detects draws and prompts a replay without awarding season points.

Synchronized UI: When the host starts a new round, the win popup closes for all connected players.

Responsive Design: Optimized for mobile "Bingo-style" vertical play and desktop browsers.

🚀 How to Play
Start a Game: Open the HTML file in any modern browser. You are automatically assigned as the Host.

Invite Friends: Click the "Copy Invite Link 🔗" button and send the URL to your friends.

Joining: When players click your link, they will automatically connect to your session.

Gameplay: Players take turns flipping two cards. If they match a team logo, they earn a point and go again. If not, the turn passes to the next player.

Winning: The player with the most pairs at the end wins the round and earns a Season Win on the leaderboard.

🛠️ Technical Stack
Frontend: HTML5, CSS3 (Flexbox/Grid), Vanilla JavaScript.

Networking: PeerJS (WebRTC) for peer-to-peer data synchronization.

Visual Effects: Canvas-Confetti for victory celebrations.

Icons: Official team logos sourced via Wikimedia Commons SVG repository.

📂 Installation & Deployment
Since this is a client-side application, no backend installation is required.

Download the index.html file.

Host it on any static web host (GitHub Pages, Netlify, Vercel) or simply run it locally.

Note: For PeerJS to work across different networks, HTTPS is highly recommended.

⚙️ Configuration
The game handles logic through a central gameState object managed by the Host:

JavaScript
let gameState = {
    cards: [],        // Array of card objects (id, image, status)
    players: {},      // Map of PeerIDs to player profiles (names, scores, totalWins)
    playerOrder: [],  // Turn sequence
    turnIndex: 0,     // Current active player
    isProcessing: false // Prevents clicking during card-flip animations
};
⚖️ License
This project is for educational and recreational use. Team logos are trademarks of their respective leagues (NFL, NBA, MLB).
