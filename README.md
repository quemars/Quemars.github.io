# Global Time App

A simple web app that shows the current local time for cities around the world.  
Built as a CS351 project and hosted via GitHub Pages at:

> https://quemars.github.io (after pushing `index.html` on the `main` branch)

---

## Project Goal

Build a friendly, browser-based app that:

- Displays local time for a chosen city and updates every second  
- Allows selecting one city from a dropdown (basic requirement)  
- Enhanced: lets you add/remove multiple cities to track at once  
- Enhanced: supports a light/dark theme toggle

---

## Features

### Basic

- Dropdown to choose a city (e.g., Los Angeles, New York, London, Tokyo, etc.)
- “Current Selected City” card that:
  - Shows the city name
  - Updates the time every second using JavaScript and `setInterval`
- Time is calculated with `toLocaleTimeString` and a specific `timeZone`, not by manually adding offsets.

### Enhanced

- **Saved Cities section**
  - Click “Add City” to add the currently selected city to a list
  - Each city is shown in its own card with a live-updating clock
  - You can remove a city using the ✕ button on its card

- **Dark / Light Theme**
  - Toggle button on top switches between light and dark mode
  - Implemented by toggling a `.dark` class on `<body>` and changing colors in CSS

---

## Tech Stack

- **HTML** – structure and layout
- **CSS** – styling and basic responsiveness
- **JavaScript** – DOM manipulation, time calculations, and live updates

No external libraries or frameworks are required.

---

## How It Works

### Time Calculation

The app uses the browser’s built-in internationalization API:

```js
new Date().toLocaleTimeString("en-US", {
  timeZone: "Europe/London",
  hour12: false
});

https://quemars.github.io
