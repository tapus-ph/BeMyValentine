# 💖 Be My Valentine - Interactive Valentine's Day Website

A fun, playful, and fully customizable 8-bit/pixelated themed Valentine's Day proposal website with an interactive "No" button that refuses to let them say no!

![Valentine's Day](https://img.shields.io/badge/Valentine's%20Day-💖-ff69b4)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🎮 Live Demo

Visit the configuration page: [Create Your Valentine](https://achllzvr.github.io/BeMyValentine/)

## ✨ Features

### 🎨 Fully Customizable
- **Custom Messages** - Personalize both question and success messages
- **Color Themes** - Choose your own 3-color palette
- **Live Preview** - See changes in real-time before sharing
- **URL Sharing** - All configurations encoded in shareable URL

### 🎭 Interactive "No" Button (10 Variations!)
1. **Teleports** - Moves randomly around the screen
2. **Shrinks** - Gets smaller with each click
3. **Shakes** - Nervous trembling
4. **Text Change** - Displays desperate messages ("Wait!", "Stop!", "Why?!")
5. **Grows Yes Button** - Makes the Yes button bigger
6. **Spins** - Rotates randomly (dizzy effect)
7. **Color Change** - Blushes pink/red
8. **Tries to Hide** - Fades out (but you can still click it!)
9. **Position Swap** - Switches places with Yes button
10. **Vibrates** - Panics with rapid shaking

### 💬 30 Hilarious Messages
Rotating messages include:
- "The No button is lava! 🔥"
- "Error 404: Love not found 🤖"
- "My cat is judging you 🐱"
- "I made you a website! 🎨"
- "Resistance is futile! 🛸"
- And 25 more!

### 🎉 Success Celebration
- Custom success message
- Colorful fireworks animation
- Floating hearts everywhere
- Bouncing celebration title

### 🌊 Beautiful Animations
- Animated gradient background that waves and shifts
- Floating hearts that rise and pop
- All animations use your custom color scheme
- Smooth transitions and effects

### 📱 Responsive Design
- Works perfectly on desktop, tablet, and mobile
- Dynamic card sizing (expands when memes appear)
- Viewport-aware button positioning (No button never goes off-screen)

## 🚀 Quick Start

### Option 1: Use the Live Site
1. Visit [https://achllzvr.github.io/BeMyValentine/](https://achllzvr.github.io/BeMyValentine/)
2. Customize your message, colors, and text
3. Click "Generate Link!"
4. Share the generated URL with your Valentine 💕

### Option 2: Run Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/achllzvr/BeMyValentine.git
   cd BeMyValentine
   ```

2. Open `index.html` in your browser

3. That's it! No build process required.

## 📁 Project Structure

```
BeMyValentine/
├── index.html          # Redirect to valentine.html
├── valentine.html      # Main application
├── memes/              # Your meme images folder
│   ├── sad-cat-1.jpg
│   ├── pleading-cat.jpg
│   └── ...
├── CNAME              # Custom domain configuration (optional)
└── README.md          # This file
```

## 🖼️ Adding Custom Memes

1. Create a `memes` folder in the project directory
2. Add your funny sad/pleading meme images
3. Update the `memeImages` array in `valentine.html` (around line 450):

```javascript
const memeImages = [
    'memes/sad-cat-1.jpg',
    'memes/pleading-cat.jpg',
    'memes/crying-cat.jpg',
    'memes/puppy-eyes.jpg',
    // Add your own memes here!
];
```

### Recommended Meme Types
- Sad cats with big eyes
- Puss in Boots pleading eyes
- Crying cat memes
- Puppy dog eyes
- "But why?" memes
- Any cute animal looking sad

## 🎨 How It Works

### Configuration Screen
When you first open the site, you'll see:
- Form to input your custom question
- Textarea for success message
- Three color pickers for your theme
- **Live preview** with toggle between Question/Success views
- Generate button to create shareable link

### Generated Link
The URL contains encoded parameters:
```
valentine.html?q=Your+Question&s=Success+Message&c1=%23FFE5EC&c2=%23FF69B4&c3=%23FFFFFF
```

Parameters:
- `q` - Question message
- `s` - Success message  
- `c1` - Color 1 (Light/accent)
- `c2` - Color 2 (Main/primary)
- `c3` - Color 3 (Background/card)

### User Experience
1. Recipient opens your custom link
2. Sees your personalized question with custom colors
3. Tries to click "No" → Button plays around!
4. Each click shows a new meme and funny message
5. Eventually clicks "Yes" → 🎉 Celebration with fireworks!

## 🌐 Deployment

### GitHub Pages (Free!)

1. Fork or clone this repository
2. Go to **Settings** → **Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Click **Save**
5. Your site will be live at: `https://yourusername.github.io/BeMyValentine/`

### Custom Domain (Optional)

1. Purchase a domain (e.g., from Namecheap, Google Domains)
2. Update the `CNAME` file with your domain
3. Configure DNS records at your registrar:
   ```
   Type: A     Name: @     Value: 185.199.108.153
   Type: A     Name: @     Value: 185.199.109.153
   Type: A     Name: @     Value: 185.199.110.153
   Type: A     Name: @     Value: 185.199.111.153
   Type: CNAME Name: www   Value: yourusername.github.io
   ```
4. Enable custom domain in GitHub Pages settings

## 🛠️ Customization Guide

### Changing Default Colors
Edit the CSS variables in `valentine.html`:
```css
:root {
    --color1: #FFE5EC;  /* Light/accent */
    --color2: #FF69B4;  /* Main/primary */
    --color3: #FFFFFF;  /* Background */
}
```

### Adding More Button Behaviors
Find the behavior cycle (around line 480) and add your own:
```javascript
} else if (behavior === 10) {
    // Your custom behavior here!
}
```

### Customizing Messages
Edit the `messages` array (around line 460):
```javascript
const messages = [
    "Your custom message here! 😊",
    // Add more messages...
];
```

## 💡 Pro Tips

1. **Test Your Link** - Always click your generated link to preview before sharing
2. **Keep Messages Short** - Shorter messages look better on mobile
3. **High Contrast Colors** - Ensure Color 2 and Color 3 contrast well for readability
4. **Compress Memes** - Keep meme images under 1MB for faster loading
5. **Mobile First** - Test on mobile devices before sharing

## 🤝 Contributing

Contributions are welcome! Here are some ideas:
- Add more button variations
- Create new message templates
- Improve mobile responsiveness
- Add sound effects
- Create themes/presets

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 💖 Credits

Created with love for Valentine's Day! Feel free to fork, customize, and share.

**Special thanks to:**
- Press Start 2P font by CodeMan38
- All the meme creators out there
- Everyone celebrating love! 💕

## 🐛 Troubleshooting

**Memes not showing?**
- Check that the `memes` folder exists
- Verify image filenames match the array exactly
- Ensure files are in supported formats (.jpg, .png, .gif)

**Colors not applying?**
- Use the generated URL (with parameters)
- Check that color values are valid hex codes
- Clear browser cache and refresh

**Link too long?**
- Use shorter messages
- Consider a URL shortener (bit.ly, tinyurl)
- The link will still work even if long!

**No button going off-screen?**
- This should be fixed! The button stays within viewport bounds
- If you still see issues, please open an issue on GitHub

## 📞 Support

Having issues? Found a bug?
- Open an issue on GitHub
- Check existing issues for solutions
- Contribute fixes via pull requests

---

Made with 💖 for Valentine's Day

**⭐ If you like this project, please give it a star!**