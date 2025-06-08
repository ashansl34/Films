# FilmFlix - A Modern Streaming Website Demo

This project is a fully client-side film streaming website demo built with pure HTML, CSS, and JavaScript, served by a simple Node.js/Express server. It showcases a modern, responsive design with a dark theme, real-time search, and a modal video player.

## Features

- **Responsive Design**: Mobile-friendly grid layout that adapts to any screen size.
- **SaaS-Style UI**: A professional look with a hero section, process cards, and a clean footer.
- **Six Film Categories**: Pre-defined sections for different languages.
- **YouTube Integration**: Film cards automatically fetch YouTube thumbnails and use an embedded player.
- **Custom Modal Player**: A clean, focused viewing experience without leaving the page.
- **Real-Time Search**: Instantly filter all films by title as you type.
- **Ad Placeholders**: Demonstrates where banner ads can be placed.
- **Zero Dependencies (Front-End)**: The `index.html` file is self-contained with no external CSS or JS libraries.

## Prerequisites

- [Node.js](https://nodejs.org/) (which includes npm) must be installed on your machine.

## How to Get Started

### 1. Download or Clone the Project

Download the `index.html`, `server.js`, and this `readme.md` file and place them in a new project folder.

### 2. Install Dependencies

Open a terminal or command prompt in your project folder and run the following command to install Express, the only dependency for the server:

```bash
npm install express
```

This will create a `node_modules` folder and a `package-lock.json` file.

### 3. Run the Server

Start the application by running the `server.js` file:

```bash
node server.js
```

You should see a message in your terminal:
`🚀 Server is running on http://localhost:3000`

### 4. View the App

Open your web browser and navigate to [http://localhost:3000](http://localhost:3000).

---

## How to Add or Change Films (Admin)

Since this is a front-end-only application, adding new films is done by manually editing the `index.html` file.

1.  **Find the YouTube Video ID**: For any YouTube video, the ID is the string of characters after `v=` in the URL.
    -   Example URL: `https://www.youtube.com/watch?v=COv52Qyctws`
    -   Video ID: `COv52Qyctws`

2.  **Edit `index.html`**: Open the file in a code editor.

3.  **Locate the Category**: Find the appropriate category section (e.g., `<section id="sinhala" ...>`).

4.  **Copy and Paste a Film Card**: Copy an existing `<div class="film-card">...</div>` block.

5.  **Update the Data**: Change the `data-title` and `data-video-id` attributes in the new block. The thumbnail will update automatically.

**Example Film Card Structure:**

```html
<!-- Add this block inside a .film-grid div -->
<div class="film-card" data-title="YOUR FILM TITLE" data-video-id="YOUTUBE_VIDEO_ID">
    <img src="https://img.youtube.com/vi/YOUTUBE_VIDEO_ID/hqdefault.jpg" alt="Thumbnail" class="film-thumbnail">
    <div class="film-info">
        <h3 class="film-title">YOUR FILM TITLE</h3>
        <button class="watch-btn">Watch Now</button>
    </div>
</div>
```
