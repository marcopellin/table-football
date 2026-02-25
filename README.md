# ⚽ Foosball Tournament Generator

A web application to organize and manage foosball tournaments with a touch-optimized interface for mobile devices.

![Version](https://img.shields.io/badge/version-5.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## 🎯 Features

- **Automatic tournament generation**: Create 1 or 4 sequential tournaments with intelligent team rotation
- **Fullscreen touch interface**: Landscape-optimized mode for scoring goals with direct taps
- **Live standings during match**: Real-time tournament standings updated with current match score in the bottom half of the screen
- **Red vs Blue color system**: Visual team identification with automatic side switching
- **Goal difference tracking**: Complete standings with goals for, goals against, and goal difference
- **Odd player management**: "Pippo" system for tournaments with an odd number of players
- **Real-time scoring**: Large tappable squares to score goals quickly with color-coded teams
- **Auto-advance**: Automatically moves to the next match after each game
- **Automatic standings**: Automatic calculation of wins, losses, and goal statistics
- **Tournament victory screen**: Celebratory screen showing the tournament winner
- **Data persistence**: Automatic player data saving in the browser
- **Best of 3 support**: Special mode for 2-team tournaments with game-by-game tracking

## 📱 Screenshots

### Main View
Player management and tournament generation with an intuitive interface showing complete standings with goal statistics.

### Fullscreen Mode
Two large color-coded squares (red vs blue) to score goals with a tap - perfect for fast-paced games!

## 🚀 How to Use

1. **Open the file**: Simply open `index.html` in your browser
2. **Add players**: Enter player names (or use the pre-loaded ones)
3. **Select participants**: Choose at least 4 players for the tournament
4. **Generate tournaments**: Click on "Generate 4 Tournaments" or "Generate 1 Tournament"
5. **Play**: Tap on a match to open fullscreen mode
6. **Score goals**: Tap on a team's colored square to add a goal
7. **Swap colors** (optional): Use "🔄 Inverti Colori" button to switch team sides
8. **Confirm victory**: When a team reaches the goal limit, confirm and move to the next match

## 🎮 Fullscreen Mode

### Layout:
- **Top half (50%)**: Color-coded team squares for scoring
- **Bottom half (50%)**: Live tournament standings with current match score included

### How it works:
- **Red team (left)**: Tap the red square to add a goal
- **Blue team (right)**: Tap the blue square to add a goal
- **"−" button**: Removes 1 goal (in case of error)
- **First to 5 wins** (or 10 for Best of 3): The square lights up green when a team wins
- **Mandatory confirmation**: Prevents accidental errors
- **Auto-advance**: To the next match after confirmation
- **Automatic side switching**: Teams that play consecutively automatically switch sides
- **Live standings update**: Every goal scored immediately updates the standings with current match included

### Color System:
- 🔴 **Red team (left side)**: Defense position
- 🔵 **Blue team (right side)**: Attack position
- Teams automatically switch sides when playing consecutive matches
- Manual swap available via "🔄 Inverti Colori" button

### Live Standings:
- 🎯 Current match teams highlighted in yellow
- 📊 Real-time calculation includes current match score
- 🏆 Tournament winner highlighted when all matches complete
- Automatic position updates as goals are scored

### Recommended:
- 📱 Use your phone in **landscape mode**
- 🔊 Volume up for tournament atmosphere
- 👥 Teams stay on their chosen color throughout the tournament
- 📊 Monitor standings live as you play

## 🏆 Tournament Formats

### 2 Teams
- Best of 3 (2 wins out of 3)
- Each match to 10 goals
- Automatic side switching between games
- Detailed game-by-game results displayed

### 3 Teams
- Round-robin
- Every team plays against all others
- Matches to 5 goals
- Automatic side switching for consecutive matches

### 4 Teams
- 2 Semifinals
- 3rd/4th place final
- 1st/2nd place final
- Matches to 5 goals
- Dynamic bracket updates (placeholders replaced with actual teams)

### 5+ Teams
- Round-robin
- Every team plays against all others
- Matches to 5 goals
- Intelligent match ordering to minimize consecutive plays
- Automatic side switching when playing consecutive matches

## 📊 Standings & Statistics

The standings table shows:
- **V** (Vittorie/Wins): Number of matches won
- **P** (Perse/Losses): Number of matches lost
- **GF** (Goal Fatti/Goals For): Total goals scored
- **GS** (Goal Subiti/Goals Against): Total goals conceded
- **DR** (Differenza Reti/Goal Difference): GF - GS

Teams are ranked by:
1. Wins (most wins first)
2. Goal Difference (highest first)
3. Losses (fewest first)

The tournament winner is automatically highlighted with 🏆 and green background when all matches are complete.

## 🤖 "Pippo" System

With an odd number of players, a virtual player called **Pippo** is created:

- Pippo's partner varies from tournament to tournament
- In matches, Pippo is substituted by another player
- Rotation is automatic and balanced
- Prevents the same player from always substituting Pippo

## 💾 Data Saving

- Players are automatically saved in the browser's `localStorage`
- Team color preferences persist throughout each tournament
- Data persists between sessions
- No server required - everything works offline

## 🛠️ Technologies

- **HTML5**: Semantic structure with PWA support
- **CSS3**: Responsive design with flexbox, grid, and color-coded teams
- **Vanilla JavaScript**: No external dependencies
- **LocalStorage API**: Client-side data persistence

## 📋 Pre-loaded Players

The application includes these example players:
- Marco, Alessio, Alessandro, Andrea, Michele
- Enrico, Martin, Massimo, Karim, Vincenzo

You can remove them or add others as you wish.

## 🎨 Customization

### Change goals to win:
In the code, modify the variable in the `buildMatches()` function:
```javascript
const goalsToWin = (numTeams === 2) ? 10 : 5;
```

### Change team colors:
Modify the color classes in CSS:
```css
.red { border: 4px solid #d32f2f; }
.blue { border: 4px solid #1976d2; }
```

### Modify number of tournaments:
```javascript
createSequentialTournaments(4); // Change the number here
```

## 🌐 Browser Compatibility

- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari (iOS/macOS)
- ✅ Opera
- ⚠️ IE11 (limited, not supported)

**Note**: Fullscreen mode works best on modern mobile devices. The app uses `100dvh` for optimal mobile display.

## 📱 PWA Features

- Custom app icon (⚽) when saved to home screen
- Optimized for mobile with proper viewport settings
- Works offline after first load
- Theme color for status bar integration

## 📝 Roadmap

- [ ] Improve 5+ matches
- [ ] Multi-language support (i18n)
- [ ] Historical statistics per player
- [ ] Export results to PDF/CSV
- [ ] "Quick tournament" mode (3 goals)
- [ ] Match timer
- [ ] Goal sound effects
- [ ] Dark mode
- [ ] Full PWA with service worker
- [ ] Online multiplayer

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the project
2. Create a branch for your feature (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is released under the MIT License. See the `LICENSE` file for details.

## 👤 Author

Created with ❤️ for foosball enthusiasts

## 🙏 Acknowledgments

- Thanks to all the players who tested the app
- Inspired by foosball nights at the office

## 📧 Contact

For questions, suggestions, or bug reports, open an issue on GitHub.

---

**Have fun and may the best team win!** 🏆⚽
