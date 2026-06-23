# 🎬 Movie Discovery App

A **React-based movie discovery application** that lets users browse popular movies, search for titles, and maintain a personalized favorites list. Powered by **The Movie Database (TMDB) API**.

## ✨ Features

- **Browse Popular Movies** — Fetches and displays currently popular movies on load
- **Search Movies** — Real-time search against TMDB's extensive movie database
- **Favorites Management** — Add/remove movies to your favorites with a single click
- **Persistent Storage** — Favorites are saved to `localStorage` and survive page refreshes
- **Dedicated Favorites Page** — View all your saved movies in one place
- **Responsive Grid Layout** — Clean card-based UI that works across screen sizes

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **React 19** | UI framework with hooks (`useState`, `useEffect`, `useContext`) |
| **React Router v7** | Client-side routing (`/` home, `/favorites`) |
| **Vite 7** | Fast build tool and dev server with HMR |
| **TMDB API** | Movie data source (popular movies, search) |
| **CSS** | Custom stylesheets (no CSS framework) |
| **ESLint** | Code linting and quality |

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ installed
- A TMDB API key (free from [themoviedb.org](https://www.themoviedb.org/settings/api))

### Installation

```bash
# Navigate to the project directory
cd "movie app frontend"

# Install dependencies
npm install

# Start the development server
npm run dev
```

The app will be available at `http://localhost:5173`.

### Build for Production

```bash
npm run build
npm run preview
```

## 📁 Project Structure

```
src/
├── App.jsx                   # Root component with routing
├── main.jsx                  # Entry point (BrowserRouter wrapper)
├── services/
│   └── api.js                # TMDB API calls (popular, search)
├── contexts/
│   └── MovieContext.jsx      # Global favorites state + localStorage
├── pages/
│   ├── Home.jsx              # Search bar + movie grid
│   └── Favorites.jsx         # Saved movies display
├── components/
│   ├── NavBar.jsx            # Top navigation bar
│   └── MovieCard.jsx         # Movie poster + favorite toggle
├── css/                      # Stylesheets
└── assets/                   # Static assets
```

## 🔑 API Key

The TMDB API key is located in `src/services/api.js`. Replace it with your own:

```js
const API_KEY = "your_api_key_here";
```

## 📄 License

MIT
