# NBA Scouting AI - Advanced Player Analysis Platform

A modern, minimalist AI basketball scouting application that rates college players and predicts NBA potential with interactive visualizations and animations.

![NBA Scout AI](https://img.shields.io/badge/Next.js-15.2-brightgreen) ![TypeScript](https://img.shields.io/badge/TypeScript-5.3-blue) ![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38B2AC) ![Framer Motion](https://img.shields.io/badge/Framer%20Motion-11.0-FF00FF)

## 🎯 Features

### 📊 Player Input & Data Management
- **Manual Input**: Input player stats directly via an intuitive form
- **CSV Upload**: Bulk import multiple college player statistics
- **Player Database**: Store and manage unlimited player profiles
- **Search & Filter**: Quickly find players by name, college, position, or rating

### 🤖 AI Analysis Engine
- **NBA Potential Rating**: 1-100 scale rating based on comprehensive analysis
- **Draft Projections**: Predictions for lottery pick, first round, or second round
- **Position Analysis**: AI determines best-fit NBA positions based on skills
- **Skill Ratings**: Detailed breakdown of shooting, defense, athleticism, passing, ball handling, and rebounding

### 📈 Advanced Visualizations
- **Radar Charts**: Interactive skill comparison radar
- **Career Trajectory**: 15-year career projection with peak ratings
- **Similar Players**: Comparison with historical NBA stars
- **Line Charts**: Performance metrics over predicted career arc
- **Animated Transitions**: Smooth animations on all chart updates

### ⚡ Simulation Mode
- **Draft Scenarios**: Simulate draft pick outcomes
- **Mid-Career Trade**: Project performance after a hypothetical trade
- **Ideal Lineup**: See potential in optimal team situation
- **Outcome Predictions**: Career points, efficiency, peak rating, and All-Star selections

### 💾 Profile Management
- **Save Profiles**: Store player profiles for future reference
- **Scouting Notes**: Add custom observations and analysis
- **Tag System**: Organize players with custom tags
- **Export/Import**: CSV support for data portability

### 🎨 Modern UI/UX
- **Minimalist Design**: Clean, sports-themed dashboard
- **Responsive Layout**: Optimized for mobile, tablet, and desktop
- **Dark Mode**: Eye-friendly dark color scheme throughout
- **Subtle Animations**: Page transitions, button hovers, chart animations
- **Glass Effect**: Modern glassmorphism design elements

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- npm or yarn

### Installation

1. **Clone the repository**
```bash
cd "NBA draft"
```

2. **Install dependencies**
```bash
npm install
```

3. **Run development server**
```bash
npm run dev
```

4. **Open in browser**
```
http://localhost:3000
```

## 📖 How to Use

### Scouting a Player

1. Navigate to **Scout** page
2. Fill in player information:
   - Name, college, season
   - College stats (PPG, RPG, APG, etc.)
   - Shooting percentages (FG%, 3P%, FT%)
   - Physical attributes (height, wingspan, weight)
3. Click **Analyze Player**
4. View instant AI analysis including:
   - Overall rating and draft projection
   - Skill breakdown with radar chart
   - Projected career trajectory
   - Similar NBA player comparisons

### Uploading Multiple Players

1. Prepare a CSV file with columns:
   ```
   name,college,season,points,rebounds,assists,steals,blocks,
   field_goal_percentage,three_point_percentage,free_throw_percentage,
   turnovers,height,wingspan,weight,position,scouting_notes,tags
   ```

2. On **Scout** page, click **Upload CSV**
3. Select your file
4. All players will be analyzed and saved automatically

### Managing Players

1. Go to **Players** page
2. View all scouted players in card view
3. **Filter** by position, search by name/college
4. **Sort** by rating or alphabetically
5. Click **View** to see detailed analysis
6. Add scouting notes, tags, and observations
7. Delete players you no longer need

### Running Simulations

1. Navigate to **Simulations** page
2. Select a player from dropdown
3. Choose simulation scenario:
   - **Draft Pick**: Standard draft projection
   - **Mid-Career Trade**: Effect of team change
   - **Ideal Lineup**: Best-case scenario
4. Click **Run Simulation**
5. See projected career outcomes

## 🏗️ Technology Stack

- **Frontend**: React 18 + Next.js 15
- **Language**: TypeScript 5.3
- **Styling**: Tailwind CSS 3.4
- **Animations**: Framer Motion 11.0
- **Charts**: Recharts 2.10
- **Storage**: Browser localStorage
- **Build Tool**: Turbopack (via Next.js)

## 📁 Project Structure

```
src/
├── app/
│   ├── layout.tsx              # Root layout
│   ├── page.tsx                # Home page
│   ├── globals.css             # Global styles
│   ├── scout/
│   │   └── page.tsx            # Scout page
│   ├── players/
│   │   ├── page.tsx            # Players list
│   │   └── [id]/
│   │       └── page.tsx        # Player detail
│   └── simulations/
│       └── page.tsx            # Simulation lab
├── components/
│   ├── Navigation.tsx          # Header/nav
│   ├── ScoutingForm.tsx        # Input form
│   └── AnalysisResults.tsx     # Results display
├── lib/
│   ├── ai-engine.ts            # AI analysis logic
│   └── storage.ts              # Data management
├── types/
│   └── index.ts                # TypeScript types
└── hooks/
    └── (custom hooks)
```

## 🎨 Customization

### Color Scheme
Edit `tailwind.config.ts` to modify colors:
```js
colors: {
  primary: "#0F172A",      // Change dark background
  secondary: "#1E293B",    // Change secondary background
  accent: "#3B82F6",       // Change accent color
}
```

### AI Analysis Weights
Modify `src/lib/ai-engine.ts` to adjust how ratings are calculated:
```ts
const weights = {
  shooting: 0.20,
  defense: 0.20,
  athleticism: 0.20,
  passing: 0.15,
  ballHandling: 0.15,
  rebounding: 0.10,
};
```

### Compare Players
Add more historical NBA data to `historicalNBAData` in AI engine for better comparisons

## 📊 Data Format

### Player Stats Object
```json
{
  "points": 20.5,
  "rebounds": 7.2,
  "assists": 4.1,
  "steals": 1.5,
  "blocks": 0.8,
  "fieldGoalPercentage": 0.456,
  "threePointPercentage": 0.385,
  "freeThrowPercentage": 0.812,
  "turnovers": 2.1
}
```

### Physical Attributes
```json
{
  "height": 78,        // in inches
  "wingspan": 82,      // in inches
  "weight": 215,       // in pounds
  "position": "Small Forward"
}
```

## 🎯 Features Roadmap

- [ ] Backend API integration
- [ ] Real NBA historical data import
- [ ] Advanced ML models for predictions
- [ ] Multi-player comparison charts
- [ ] Team build simulator
- [ ] Draft order generator
- [ ] Player performance tracking
- [ ] Coaching insights
- [ ] Community comparisons
- [ ] Mobile app (React Native)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available for personal and educational use.

## ⚠️ Disclaimer

All AI predictions are estimates based on historical trends and college statistics. Actual NBA performance depends on many variables not captured in this model, including:
- Coaching quality
- Team fit and chemistry  
- Injury history
- Work ethic and dedication
- NBA Draft outcome
- League evolution

Use these predictions as a tool for analysis, not as definitive projections.

## 📞 Support

For issues, questions, or feedback, please open an issue on GitHub.

---

**Built with ❤️ for basketball enthusiasts and analytics nerds**
