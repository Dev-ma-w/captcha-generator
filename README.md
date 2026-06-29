# 🔐 CAPTCHA Generator

<div align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  
  <h3>Interactive CAPTCHA Verification System</h3>
  <p>A modern, user-friendly CAPTCHA generator for web form security and bot prevention.</p>
  
  <a href="https://captcha-generator-dusky.vercel.app">🌐 Live Demo</a>
</div>

---

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Future Enhancements](#future-enhancements)
- [Author](#author)

---

## 🎯 Overview

**CAPTCHA Generator** is a modern web application that provides a secure and user-friendly CAPTCHA verification system. It prevents automated bot attacks on web forms while maintaining an excellent user experience. The generator includes multiple CAPTCHA types and customizable options.

This project demonstrates proficiency in frontend development with JavaScript interactivity and security best practices.

---

## ✨ Features

### 🔤 Multiple CAPTCHA Types
- ✅ Text-based CAPTCHA
- ✅ Image-based CAPTCHA
- ✅ Math puzzle CAPTCHA
- ✅ Slider verification

### 🎨 Customization Options
- ✅ Adjustable difficulty levels
- ✅ Custom styling
- ✅ Theme selection (light/dark)
- ✅ Language support

### 🔄 User-Friendly Features
- ✅ Refresh/regenerate CAPTCHA
- ✅ Accessibility support
- ✅ Audio alternative
- ✅ Clear instructions

### 🔒 Security Features
- ✅ Session-based validation
- ✅ Expiration time limit
- ✅ Rate limiting
- ✅ Anti-tampering measures

### 📱 Responsive Design
- ✅ Mobile-optimized
- ✅ Tablet compatible
- ✅ Desktop-friendly
- ✅ Cross-browser support

### 📊 Analytics & Logging
- ✅ Success/failure tracking
- ✅ Attempt logging
- ✅ Performance metrics
- ✅ User statistics

---

## 🛠️ Technology Stack

| Category | Technology |
|----------|-----------|
| **Frontend** | HTML5, CSS3, JavaScript (ES6+) |
| **Styling** | CSS3 Grid/Flexbox, CSS Animations |
| **Libraries** | Canvas API, Web APIs |
| **Storage** | Local Storage, Session Storage |
| **Hosting** | Vercel |
| **Version Control** | Git & GitHub |

---

## 📁 Project Structure

```
captcha-generator/
├── index.html                   # Main entry point
├── css/
│   ├── style.css               # Main stylesheet
│   ├── responsive.css          # Responsive design
│   └── themes.css              # Theme styles
├── js/
│   ├── main.js                 # Main application
│   ├── captcha-generator.js    # CAPTCHA logic
│   ├── validator.js            # Validation logic
│   └── utils.js                # Utility functions
├── assets/
│   ├── fonts/                  # Custom fonts
│   ├── icons/                  # SVG icons
│   └── images/                 # Sample images
├── docs/
│   └── api.md                  # API documentation
└── README.md                   # This file
```

---

## 🚀 Installation

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Code editor (VS Code, Sublime Text, etc.)
- Git (optional)

### Step 1: Clone the Repository
```bash
git clone https://github.com/Dev-ma-w/captcha-generator.git
cd captcha-generator
```

### Step 2: Open in Browser
Simply open `index.html` in your browser:
```bash
# Using Live Server extension in VS Code
# Or open directly
open index.html
```

### Step 3: View Live Demo
Visit the deployed version: [https://captcha-generator-dusky.vercel.app](https://captcha-generator-dusky.vercel.app)

---

## 💻 Usage

### Basic Implementation

#### HTML
```html
<div id="captcha-container"></div>
<button onclick="verifyCaptcha()">Verify</button>
```

#### JavaScript
```javascript
// Initialize CAPTCHA
const captcha = new CaptchaGenerator({
  type: 'text',
  difficulty: 'medium',
  theme: 'light'
});

// Render CAPTCHA
captcha.render('#captcha-container');

// Verify user input
function verifyCaptcha() {
  const userInput = document.getElementById('captcha-input').value;
  if (captcha.verify(userInput)) {
    alert('CAPTCHA verified successfully!');
  } else {
    alert('Invalid CAPTCHA. Please try again.');
    captcha.refresh();
  }
}
```

### Configuration Options

```javascript
const options = {
  type: 'text',           // 'text', 'math', 'image', 'slider'
  difficulty: 'medium',   // 'easy', 'medium', 'hard'
  theme: 'light',         // 'light', 'dark'
  expiration: 300000,     // 5 minutes (milliseconds)
  maxAttempts: 5,         // Maximum verification attempts
  width: 300,             // Width in pixels
  height: 100,            // Height in pixels
  fontSize: 24,           // Font size
  noiseLevel: 'medium'    // 'low', 'medium', 'high'
};
```

---

## 🔌 API Documentation

### CaptchaGenerator Class

#### Constructor
```javascript
new CaptchaGenerator(options)
```

#### Methods

##### `render(selector)`
Renders the CAPTCHA in the specified DOM element.
```javascript
captcha.render('#captcha-container');
```

##### `verify(userInput)`
Verifies the user's input against the generated CAPTCHA.
```javascript
const isValid = captcha.verify(userInput);
```

##### `refresh()`
Generates a new CAPTCHA.
```javascript
captcha.refresh();
```

##### `reset()`
Resets all settings to default.
```javascript
captcha.reset();
```

##### `getImage()`
Returns the CAPTCHA as an image data URL.
```javascript
const imageUrl = captcha.getImage();
```

---

## 🎨 Customization

### Change Theme
```javascript
captcha.setTheme('dark');
```

### Adjust Difficulty
```javascript
captcha.setDifficulty('hard');
```

### Change CAPTCHA Type
```javascript
captcha.setType('math');
```

### Custom Styling
Edit `css/style.css`:
```css
.captcha-container {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}
```

---

## 📸 Screenshots

### Text CAPTCHA
![Text CAPTCHA](docs/screenshots/text-captcha.png)

### Math CAPTCHA
![Math CAPTCHA](docs/screenshots/math-captcha.png)

### Image CAPTCHA
![Image CAPTCHA](docs/screenshots/image-captcha.png)

### Success Message
![Success](docs/screenshots/success.png)

---

## 🔐 Security Considerations

- ✅ Server-side validation recommended
- ✅ Token expiration implemented
- ✅ Rate limiting suggested
- ✅ HTTPS recommended for production
- ✅ Never store CAPTCHA answer in frontend
- ✅ Implement backend verification

---

## ⚡ Performance

- ✅ Lightweight (~50KB)
- ✅ No external dependencies
- ✅ Fast rendering
- ✅ Optimized canvas drawing
- ✅ Minimal DOM manipulation

---

## 🎯 Future Enhancements

- [ ] Backend API for validation
- [ ] Database integration
- [ ] Multiple language support
- [ ] Audio CAPTCHA alternative
- [ ] Advanced analytics dashboard
- [ ] AI-resistant features
- [ ] Mobile fingerprinting
- [ ] Behavior analysis
- [ ] Integration with popular frameworks
- [ ] PWA support
- [ ] Biometric verification
- [ ] Machine learning improvements

---

## 🐛 Known Issues & Limitations

- Canvas rendering may vary across browsers
- Some accessibility features need improvement
- Math CAPTCHA limited to basic operations

---

## 📝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the **MIT License**.

---

## 🤝 Support

For support, email [manojdev3003@gmail.com](mailto:manojdev3003@gmail.com) or reach out on [LinkedIn](https://www.linkedin.com/in/dev-manoj-s-176027258/).

---

## 👨‍💻 Author

**Dev Manoj S**
- 🌐 Portfolio: [devmanoj.vercel.app](https://devmanoj.vercel.app)
- 💼 LinkedIn: [@dev-manoj-s-176027258](https://www.linkedin.com/in/dev-manoj-s-176027258/)
- 📧 Email: [manojdev3003@gmail.com](mailto:manojdev3003@gmail.com)
- 🔗 GitHub: [@Dev-ma-w](https://github.com/Dev-ma-w)

---

<div align="center">

**⭐ If you found this helpful, please consider giving it a star!**

Made with ❤️ by Dev Manoj S

</div>
