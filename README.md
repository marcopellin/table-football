# table-football

# ⚽ Foosball Tournament Generator

A web application to organize and manage foosball tournaments with a touch-optimized interface for mobile devices.

![Version](https://img.shields.io/badge/version-3.1-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## 🎯 Features

- **Automatic tournament generation**: Create 1 or 4 sequential tournaments with intelligent team rotation
- **Fullscreen touch interface**: Landscape-optimized mode for scoring goals with direct taps
- **Odd player management**: "Pippo" system for tournaments with an odd number of players
- **Real-time scoring**: Large tappable squares to score goals quickly
- **Auto-advance**: Automatically moves to the next match after each game
- **Automatic standings**: Automatic calculation of wins and losses
- **Data persistence**: Automatic player data saving in the browser

## 📱 Screenshots

### Main View
Player management and tournament generation with an intuitive interface.

### Fullscreen Mode
Two large squares to score goals with a tap - perfect for fast-paced games!

## 🚀 How to Use

1. **Open the file**: Simply open `index.html` in your browser
2. **Add players**: Enter player names (or use the pre-loaded ones)
3. **Select participants**: Choose at least 4 players for the tournament
4. **Generate tournaments**: Click on "Generate 4 Tournaments" or "Generate 1 Tournament"
5. **Play**: Tap on a match to open fullscreen mode
6. **Score goals**: Tap on a team's square to add a goal
7. **Confirm victory**: When a team reaches 5 goals, confirm and move to the next match

## 🎮 Fullscreen Mode

### How it works:
- **Tap on square**: Adds 1 goal to the team
- **"−" button**: Removes 1 goal (in case of error)
- **First to 5 wins**: The square lights up green when a team wins
- **Mandatory confirmation**: Prevents accidental errors
- **Auto-advance**: To the next match after confirmation

### Recommended:
- 📱 Use your phone in **landscape mode**
- 🔊 Volume up for tournament atmosphere
- 👥 Pass the phone between teams to score

## 🏆 Tournament Formats

### 2 Teams
- Best of 3 (2 wins out of 3)
- Each match to 10 goals

### 3 Teams
- Round-robin
- Every team plays against all others
- Matches to 5 goals

### 4 Teams
- 2 Semifinals
- 3rd/4th place final
- 1st/2nd place final
- Matches to 5 goals

### 5+ Teams
- Round-robin
- Every team plays against all others
- Matches to 5 goals

## 🤖 "Pippo" System

With an odd number of players, a virtual player called **Pippo** is created:

- Pippo's partner varies from tournament to tournament
- In matches, Pippo is substituted by another player
- Rotation is automatic and balanced
- Prevents the same player from always substituting Pippo

## 💾 Data Saving

- Players are automatically saved in the browser's `localStorage`
- Data persists between sessions
- No server required - everything works offline

## 🛠️ Technologies

- **HTML5**: Semantic structure
- **CSS3**: Responsive design with flexbox and grid
- **Vanilla JavaScript**: No external dependencies
- **LocalStorage API**: Client-side data persistence

## 📋 Pre-loaded Players

The application includes these example players:
- Marco, Alessio, Alessandro, Andrea, Michele
- Massimiliano, Enrico, Martin, Massimo, Karim, Vincenzo

You can remove them or add others as you wish.

## 🎨 Customization

### Change goals to win:
In the code, modify the variable in the `buildMatches()` function:
```javascript
const goalsToWin = (numTeams === 2) ? 10 : 5;
```

### Change colors:
Modify the gradient in CSS:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
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

**Note**: Fullscreen mode works best on modern mobile devices.

## 📝 Roadmap

- [ ] Multi-language support (i18n)
- [ ] Historical statistics per player
- [ ] Export results to PDF/CSV
- [ ] "Quick tournament" mode (3 goals)
- [ ] Match timer
- [ ] Goal sound effects
- [ ] Dark mode
- [ ] PWA (Progressive Web App)
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
