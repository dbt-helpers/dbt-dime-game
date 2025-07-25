# DBT Dime Game - Progressive Web App

A modern, mobile-friendly Progressive Web App implementation of the DBT (Dialectical Behavior Therapy) Dime Game, designed to help users determine how assertively to make requests or decline others' requests.

## 🌟 Features

### Core Functionality
- **Decision Support**: Guides users through 10 structured questions to determine appropriate assertiveness levels
- **Two Scenarios**: 
  - Making requests ("Do I ask?")
  - Declining requests ("Do I say no?")
- **Scoring System**: Uses the traditional "dime" scoring (0-10) with personalized recommendations
- **Answer Review**: Users can review and modify their responses before final results

### Progressive Web App Features
- **Offline Support**: Works without internet connection after initial load
- **Installable**: Can be installed on mobile devices and desktop computers
- **Responsive Design**: Optimized for phones, tablets, and desktop
- **Fast Loading**: Cached resources for instant startup
- **Modern UI**: Beautiful gradient design with smooth animations
- **Touch-Friendly**: Large buttons and intuitive gestures

## 🚀 Quick Start

### GitHub Pages Deployment

1. **Fork or Create Repository**
   ```bash
   git clone https://github.com/yourusername/dbt-dime-game.git
   cd dbt-dime-game
   ```

2. **Add Files**
   Copy these files to your repository:
   - `index.html` (main app file)
   - `manifest.json` (PWA manifest)
   - `sw.js` (service worker)
   - `README.md` (this file)

3. **Enable GitHub Pages**
   - Go to your repository settings
   - Scroll to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

4. **Access Your App**
   - Your app will be available at: `https://yourusername.github.io/dbt-dime-game`
   - GitHub will provide the exact URL in the Pages settings

### Local Development

1. **Simple HTTP Server**
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```

2. **Open Browser**
   - Navigate to `http://localhost:8000`
   - The app will work locally with full PWA features

## 📱 Installation

### Mobile Devices
1. Open the app in your mobile browser
2. Look for "Add to Home Screen" or "Install" prompt
3. Follow the installation prompts
4. The app will appear on your home screen like a native app

### Desktop
1. Open the app in Chrome, Edge, or Safari
2. Look for the install icon in the address bar
3. Click "Install" when prompted
4. The app will be available in your applications folder

## 🎯 How to Use

### Getting Started
1. **Choose Your Scenario**
   - Select "Ask someone for something" if you're considering making a request
   - Select "Decline someone's request" if you're considering saying no

2. **Answer Questions**
   - You'll be presented with 10 yes/no questions
   - Answer honestly based on your specific situation
   - Each answer contributes to your final "dime" score

3. **Review Results**
   - Receive a personalized recommendation (0-10 dimes)
   - Review your answers and modify if needed
   - Higher scores indicate more assertive approaches

### Example Scenarios

**Making a Request (Ask)**
- Score 0-2 dimes: "Don't ask; don't hint"
- Score 5-6 dimes: "Ask gracefully, but take no"
- Score 9-10 dimes: "Ask and don't take no for an answer"

**Declining a Request (Say No)**
- Score 0-2 dimes: "Do what the other person wants without being asked"
- Score 5-6 dimes: "Say you'd rather not, but do it gracefully"
- Score 9-10 dimes: "Don't do it"

## 🏗️ Technical Details

### Architecture
- **Frontend**: Vanilla JavaScript with React (CDN)
- **Styling**: Tailwind CSS for responsive design
- **PWA**: Service Worker for offline functionality
- **Storage**: Local state management (no backend required)

### Browser Support
- **Mobile**: iOS Safari 11.3+, Android Chrome 67+
- **Desktop**: Chrome 67+, Firefox 63+, Safari 11.1+, Edge 79+

### Performance
- **First Load**: ~200KB (including all dependencies)
- **Subsequent Loads**: Instant (cached)
- **Offline**: Full functionality available

## 🔧 Customization

### Modifying Questions
Edit the `prompts` object in `index.html` to customize questions:

```javascript
const prompts = {
    ask: [
        { name: 'Custom Category', question: 'Your custom question?' },
        // ... more questions
    ],
    sayNo: [
        // ... sayNo questions
    ]
};
```

### Modifying Results
Edit the `results` object to customize recommendations:

```javascript
const results = {
    ask: [
        'Custom result for 0 dimes',
        'Custom result for 1 dime',
        // ... up to 10 dimes
    ]
};
```

### Styling
- Modify CSS custom properties in the `<style>` section
- Adjust Tailwind classes throughout the components
- Update colors in `manifest.json` for theme consistency

## 📖 About DBT Dime Game

The Dime Game is a tool from Dialectical Behavior Therapy (DBT) Interpersonal Effectiveness module, described in:

- **DBT® Skills Training Handouts and Worksheets, Second Edition** by Marsha M. Linehan
- Pages 176-177 of the manual

### Purpose
Help individuals determine the appropriate level of assertiveness when:
- Making requests of others
- Declining others' requests
- Maintaining relationships while meeting personal needs

### Therapeutic Context
This tool is part of the DEAR MAN, GIVE, and FAST skills in DBT, designed to improve interpersonal effectiveness while balancing:
- **Objectives**: Getting what you want
- **Relationships**: Maintaining positive connections
- **Self-Respect**: Feeling good about yourself

## 🤝 Contributing

### Bug Reports
Please report issues with:
- Device/browser information
- Steps to reproduce
- Expected vs actual behavior

### Feature Requests
Consider submitting:
- Use case descriptions
- Implementation suggestions
- Screenshots/mockups if applicable

### Development
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test across devices
5. Submit a pull request

## 📄 License

This project is licensed under the ISC License - see the original DBT materials for therapeutic use guidelines.

### Attribution
- Original DBT Dime Game concept by Marsha M. Linehan
- Progressive Web App implementation
- Based on DBT® Skills Training materials

## 🆘 Support

### Resources
- [DBT Dime Game Worksheet](https://borderlinebabble.com/2015/12/08/dbt-skills-group-interpersonal-effectiveness-weeks-5-6/)
- [DBT Skills Training Manual](https://www.amazon.com/Skills-Training-Handouts-Worksheets-Second/dp/1572307811)

### Technical Support
For technical issues with this PWA implementation:
1. Check the browser console for errors
2. Verify PWA installation
3. Clear cache and reload
4. Report issues on GitHub

---

**Disclaimer**: This app is an educational tool and should not replace professional therapeutic guidance. For comprehensive DBT training, consult qualified mental health professionals.
