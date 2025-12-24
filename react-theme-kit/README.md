# react-theme-kit

A lightweight, plug-and-play React theme switcher that enables **Light / Dark mode** using Context API.

Perfect for beginners and production apps — just import and use 🚀

---

## ✨ Features

* 🌗 Light & Dark theme support
* ⚡ Easy to use (Context API based)
* 🔁 Toggle theme with one function
* 💾 Theme saved in localStorage
* 🧩 Zero dependencies
* 🛠 Works with any React app (CRA, Vite, Next.js)

---

## 📦 Installation

```bash
npm install react-theme-kit
```

or

```bash
yarn add react-theme-kit
```

---

## 🚀 Quick Start (Step-by-Step)

### Step 1️⃣: Wrap your App with `ThemeProvider`

In your main file (`main.jsx` / `index.js` / `App.jsx`):

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import { ThemeProvider } from "react-theme-kit";

ReactDOM.createRoot(document.getElementById("root")).render(
  <ThemeProvider>
    <App />
  </ThemeProvider>
);
```

✅ This enables theme functionality for the entire app

---

### Step 2️⃣: Use the `useTheme` hook

Create a theme toggle button anywhere in your app:

```jsx
import { useTheme } from "react-theme-kit";

const ThemeToggle = () => {
  const { theme, toggleTheme } = useTheme();

  return (
    <button onClick={toggleTheme}>
      Switch to {theme === "light" ? "Dark" : "Light"} Mode
    </button>
  );
};

export default ThemeToggle;
```

✅ `theme` → current theme (`light` or `dark`)

✅ `toggleTheme()` → switches the theme

---

### Step 3️⃣: Add CSS for Themes

Add this CSS in your global stylesheet (`index.css` or `App.css`):

```css
body.light {
  background-color: #ffffff;
  color: #000000;
}

body.dark {
  background-color: #121212;
  color: #ffffff;
}
```

🎨 You can customize colors as per your design

---

## 🧠 How It Works (Behind the Scenes)

* Uses React Context API
* Stores theme in `localStorage`
* Automatically applies `light` or `dark` class to `<body>`
* Theme persists after page refresh

---

## 🧪 Example App Structure

```bash
src/
├── App.jsx
├── main.jsx
├── index.css
└── components/
    └── ThemeToggle.jsx
```

---

## ❓ FAQ

### Q: Does it support Tailwind?

👉 Yes. You can use `dark` class with Tailwind config.

### Q: Is it SSR safe?

👉 Best for client-side apps (Next.js support coming soon).

### Q: Can I add more themes?

👉 Yes! Multi-theme support coming in future versions.

---

## 🛣 Roadmap

* 🌐 System theme detection
* 🎨 Multiple themes
* 🌀 Smooth transitions
* ⚙ Tailwind plugin support

---

## 👨‍💻 Author

Uttam Kumar
Frontend / MERN Stack Developer

---

## ⭐ Support

If you like this package, give it a ⭐ on GitHub and share it with others 🙌

Happy coding! 💙
