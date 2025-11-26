# ⚡ Live Code Editor

A powerful, browser-based code editor with real-time preview. Write HTML, CSS, and JavaScript and see results instantly. Perfect for learning, prototyping, and teaching web development.

## 🚀 Live Demo
[View Live Demo](#) <!-- Add your deployed link -->

## ✨ Features

### Editor Capabilities
- **Multi-Language Support**: Separate editors for HTML, CSS, and JavaScript
- **Live Preview**: Real-time rendering as you type (500ms debounce)
- **Tab System**: Easy switching between languages
- **Syntax Highlighting**: Dark theme for comfortable coding
- **Auto-Run**: Automatic preview updates on code changes

### Functionality
- **Run Code**: Manual execution with Run button
- **Clear Editor**: Quick reset for current tab
- **Download**: Export complete HTML file with all code
- **Refresh Preview**: Force preview reload
- **Responsive Design**: Works on all screen sizes

### User Experience
- **Beautiful Gradient UI**: Modern purple gradient theme
- **Smooth Animations**: Polished interactions and transitions
- **Intuitive Layout**: Split-screen editor and preview
- **Default Templates**: Starter code to demonstrate functionality

## 🛠️ Technologies Used

- **Vanilla JavaScript**: Pure JS, no framework dependencies
- **HTML5**: Semantic markup and iframe for preview
- **CSS3**: Modern gradients, flexbox, and animations
- **LocalStorage Ready**: Easy to extend with code persistence

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/live-code-editor.git

# Navigate to directory
cd live-code-editor

# Open in browser
open index.html
# or
python -m http.server 8000
```

No build process required! Just open `index.html` in any modern browser.

## 💻 Usage

### Basic Workflow
1. Select a tab (HTML, CSS, or JavaScript)
2. Write your code in the editor
3. Watch the live preview update automatically
4. Click "Run" for manual refresh
5. Download your complete project

### Example Projects to Try

**Animated Card**
```css
/* CSS Tab */
.card {
  width: 300px;
  padding: 30px;
  background: linear-gradient(135deg, #667eea, #764ba2);
  border-radius: 20px;
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-20px); }
}
```

**Interactive Button**
```javascript
// JavaScript Tab
document.querySelector('button').addEventListener('click', () => {
  alert('Hello from Live Code Editor!');
});
```

## 🎯 Technical Implementation

### Live Preview System
```javascript
function runCode() {
  const html = document.getElementById('htmlEditor').value;
  const css = document.getElementById('cssEditor').value;
  const js = document.getElementById('jsEditor').value;

  const iframe = document.getElementById('preview');
  const doc = iframe.contentDocument;

  const fullCode = `
    <!DOCTYPE html>
    <html>
    <head><style>${css}</style></head>
    <body>
      ${html}
      <script>${js}<\/script>
    </body>
    </html>
  `;

  doc.open();
  doc.write(fullCode);
  doc.close();
}
```

### Auto-Run with Debounce
```javascript
let timeout;
document.querySelectorAll('.editor').forEach(editor => {
  editor.addEventListener('input', () => {
    clearTimeout(timeout);
    timeout = setTimeout(runCode, 500);
  });
});
```

## 🎨 UI Highlights

- **Gradient Theme**: Purple gradient (`#667eea` to `#764ba2`)
- **Dark Code Editor**: `#1e1e1e` background for reduced eye strain
- **Smooth Transitions**: 0.3s transitions on all interactive elements
- **Hover Effects**: Scale and shadow on buttons
- **Responsive Layout**: Flexbox-based adaptive design

## 🌟 Use Cases

### For Developers
- Quick prototyping and experimentation
- Code snippet testing
- Teaching tool for tutorials
- Interview preparation

### For Students
- Learning HTML, CSS, JavaScript
- Completing coding assignments
- Building small projects
- Understanding how code works together

### For Educators
- Live coding demonstrations
- Interactive teaching material
- Student code review
- Real-time collaboration (with extension)

## 🚀 Future Enhancements

- [ ] Code syntax highlighting with libraries (Prism.js/Highlight.js)
- [ ] Multiple file support
- [ ] Code formatting (Prettier integration)
- [ ] Console output panel
- [ ] Error detection and display
- [ ] Code sharing via URL
- [ ] Template library
- [ ] Dark/light theme toggle
- [ ] LocalStorage code persistence
- [ ] Import external libraries
- [ ] Vim/Emacs keybindings
- [ ] Code collaboration features

## 📚 Learning Outcomes

This project demonstrates:
- **DOM Manipulation**: Direct DOM access and iframe control
- **Event Handling**: Keyboard and mouse event management
- **Debouncing**: Performance optimization technique
- **Blob API**: File generation and download
- **iframe Security**: Safe code execution in sandboxed environment
- **Responsive Design**: Mobile-first CSS
- **UI/UX Design**: Clean, intuitive interfaces

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

MIT License - feel free to use this in your own projects!

## 👨‍💻 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your Name](https://linkedin.com/in/yourprofile)
- Portfolio: [yourwebsite.com](https://yourwebsite.com)
- Twitter: [@yourhandle](https://twitter.com/yourhandle)

## 🎓 Why This Project Stands Out

### For South African Developers
- **Zero Dependencies**: Works anywhere without npm/node
- **Lightweight**: Perfect for showcasing in areas with limited bandwidth
- **Educational**: Great for teaching at coding bootcamps or universities
- **Portfolio Ready**: Demonstrates core web development skills

### For International Roles
- **Clean Code**: Well-structured, readable implementation
- **Best Practices**: Modern JavaScript patterns
- **Problem Solving**: Creative solutions to preview challenges
- **Scalability**: Easy to extend with additional features

## 🔧 Browser Support

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 🙏 Acknowledgments

- Inspired by CodePen, JSFiddle, and JS Bin
- Built to demonstrate vanilla JavaScript mastery
- Perfect for technical interviews and coding assessments

## 📞 Support

If you have any questions or need help:
- Open an issue on GitHub
- Email: your.email@example.com
- LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)

---

⭐ **Star this repository** if you found it useful for your learning or portfolio!

💼 **Hiring managers**: This project showcases fundamental web development skills, clean code practices, and the ability to build practical tools from scratch.
