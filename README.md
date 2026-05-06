# 🎵 Spotify Clone

A full-stack web application that replicates Spotify's core functionality with real music playback integration using Spotify's official APIs.

[![GitHub](https://img.shields.io/badge/GitHub-Aliwael12%2Fspotify--clone-1DB954?logo=github)](https://github.com/Aliwael12/spotify-clone)
[![React](https://img.shields.io/badge/Frontend-React.js-61DAFB?logo=react)](https://reactjs.org)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?logo=node.js)](https://nodejs.org)
[![JavaScript](https://img.shields.io/badge/Language-JavaScript-F7DF1E?logo=javascript&logoColor=000)](https://www.javascript.com)
![Language Composition](https://img.shields.io/badge/JavaScript-89.3%25-F7DF1E) ![CSS](https://img.shields.io/badge/CSS-8.5%25-1572B6) ![HTML](https://img.shields.io/badge/HTML-2.2%25-E34C26)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## 🎬 Demo & Screenshots

### 🏠 Home Screen
![Home Screen](https://raw.githubusercontent.com/Aliwael12/spotify-clone/main/assets/screenshots/home-screenshot.svg)
**Features:**
- Featured playlists and recommendations
- New releases section
- Personalized suggestions based on listening history
- Quick access to your library

### 🔍 Search Results
![Search Screenshot](https://raw.githubusercontent.com/Aliwael12/spotify-clone/main/assets/screenshots/search-screenshot.svg)
**Features:**
- Real-time search functionality
- Track, artist, and playlist results
- Instant preview and play options
- Detailed track information display

### 📋 Playlist View
![Playlist Screenshot](https://raw.githubusercontent.com/Aliwael12/spotify-clone/main/assets/screenshots/playlist-screenshot.svg)
**Features:**
- Detailed playlist display with all tracks
- Artist and album information
- Play controls and queue management
- Sorting and filtering options

---

## 🏗️ System Architecture

![Architecture Diagram](https://raw.githubusercontent.com/Aliwael12/spotify-clone/main/assets/diagrams/architecture.svg)

### Architecture Overview:
1. **Client Layer** - React-based frontend with interactive UI components
2. **API Layer** - Express.js server handling HTTP requests and business logic
3. **Service Layer** - OAuth 2.0 authentication, token management, and request processing
4. **External APIs** - Integration with Spotify Web API and WebPlayback API

---

## 🛠️ Tech Stack

![Tech Stack](https://raw.githubusercontent.com/Aliwael12/spotify-clone/main/assets/diagrams/tech-stack.svg)

### Frontend Stack (89.3% JavaScript)
- **⚛️ React.js** - Component-based UI framework
- **💅 CSS3** - Responsive and modern styling
- **📄 HTML5** - Semantic markup
- **🌐 HTTP Client** - Axios/Fetch API for backend communication

### Backend Stack
- **🟢 Node.js** - Server runtime environment
- **⚡ Express.js** - Web framework for routing and middleware
- **🔐 OAuth 2.0** - Secure authentication with Spotify
- **🔄 Middleware** - CORS, body parsing, request validation

### External APIs
- **🎵 Spotify Web API** - Track/playlist search, user data, recommendations
- **▶️ Spotify WebPlayback API** - Audio playback control
- **🔑 OAuth 2.0** - Secure authorization and token management

---

## ✨ Features

- ✅ **Real-time Music Search** - Search songs, artists, albums, and playlists instantly
- ✅ **Music Playback** - Full playback control with Spotify WebPlayback API
- ✅ **User Authentication** - Secure OAuth 2.0 login with Spotify
- ✅ **Playlist Management** - View, create, and manage playlists
- ✅ **User Library** - Access saved tracks and playlists
- ✅ **Personalized Recommendations** - AI-powered suggestions based on listening habits
- ✅ **Volume Control** - Full audio control features
- ✅ **Progress Seeking** - Jump to any point in a track
- ✅ **Responsive Design** - Works on desktop, tablet, and mobile
- ✅ **Now Playing Display** - Real-time track information
- ✅ **Album Artwork** - High-quality cover art display
- ✅ **User Profile** - View profile information and stats
- ✅ **Dark Theme** - Eye-friendly dark UI (Spotify-style)

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn package manager
- Spotify Developer Account (free)
- Git

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/Aliwael12/spotify-clone.git
cd spotify-clone
```

2. **Install dependencies:**
```bash
# Frontend
npm install

# Backend (if in separate directory)
cd backend
npm install
cd ..
```

3. **Create Spotify Application:**
   - Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
   - Log in or create an account
   - Create a new application
   - Accept the terms and create the app
   - Copy your **Client ID** and **Client Secret**

4. **Set up environment variables:**

Create a `.env` file in the root directory:
```env
REACT_APP_SPOTIFY_CLIENT_ID=your_client_id_here
REACT_APP_SPOTIFY_REDIRECT_URI=http://localhost:3000/callback

# Backend
SPOTIFY_CLIENT_ID=your_client_id_here
SPOTIFY_CLIENT_SECRET=your_client_secret_here
SPOTIFY_REDIRECT_URI=http://localhost:3000/callback
NODE_ENV=development
PORT=5000
```

5. **Start the development servers:**

```bash
# Terminal 1 - Frontend (Port 3000)
npm start

# Terminal 2 - Backend (Port 5000)
cd backend
npm start
```

6. **Open your browser:**
```
http://localhost:3000
```

---

## 📁 Project Structure

```
spotify-clone/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── Header.js
│   │   ├── Sidebar.js
│   │   ├── Player.js
│   │   ├── SearchBar.js
│   │   ├── Playlist.js
│   │   └── Track.js
│   ├── pages/
│   │   ├── Home.js
│   │   ├── Search.js
│   │   ├── Login.js
│   │   └── Playlist.js
│   ├── services/
│   │   ├── spotifyService.js
│   │   ├── authService.js
│   │   └── apiClient.js
│   ├── styles/
│   │   ├── index.css
│   │   ├── components.css
│   │   └── player.css
│   ├── App.js
│   └── index.js
├── backend/
│   ├── routes/
│   │   ├── auth.js
│   │   ├── search.js
│   │   ├── playlists.js
│   │   └── user.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── errorHandler.js
│   ├── config/
│   │   └── spotify.js
│   └── server.js
├── assets/
│   ├── screenshots/
│   │   ├── home-screenshot.svg
│   │   ├── search-screenshot.svg
│   │   └── playlist-screenshot.svg
│   └── diagrams/
│       ├── architecture.svg
│       └── tech-stack.svg
├── .env.example
├── package.json
└── README.md
```

---

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/login` - Login with Spotify
- `GET /api/auth/callback` - OAuth callback handler
- `POST /api/auth/refresh` - Refresh access token
- `GET /api/auth/logout` - Logout user

### Search
- `GET /api/search?q=query&type=track,artist,playlist` - Search Spotify
- `GET /api/search/tracks?q=query` - Search tracks only
- `GET /api/search/artists?q=query` - Search artists only
- `GET /api/search/playlists?q=query` - Search playlists only

### User
- `GET /api/user/profile` - Get user profile
- `GET /api/user/top-tracks` - Get user's top tracks
- `GET /api/user/top-artists` - Get user's top artists
- `GET /api/user/saved-tracks` - Get user's saved tracks

### Playlists
- `GET /api/playlists/featured` - Get featured playlists
- `GET /api/playlists/:id` - Get playlist details
- `GET /api/playlists/:id/tracks` - Get playlist tracks
- `POST /api/playlists` - Create new playlist
- `PUT /api/playlists/:id` - Update playlist

### Playback
- `POST /api/player/play` - Start playback
- `POST /api/player/pause` - Pause playback
- `POST /api/player/next` - Skip to next track
- `POST /api/player/previous` - Go to previous track
- `PUT /api/player/volume` - Set volume level

---

## 🧪 Testing

### Running Tests
```bash
npm test
```

### Test Coverage
```bash
npm run test:coverage
```

### Manual Testing Checklist
- [ ] Login/Logout functionality
- [ ] Search functionality (tracks, artists, playlists)
- [ ] Playback controls (play, pause, skip, volume)
- [ ] Playlist viewing and navigation
- [ ] Responsive design on mobile devices
- [ ] Proper error handling

---

## 🐛 Troubleshooting

### Issue: "Invalid Client ID"
**Solution:** Verify your Spotify Client ID in `.env` file and ensure it matches your application settings.

### Issue: "Redirect URI Mismatch"
**Solution:** Add your redirect URI to your Spotify app settings:
1. Go to Spotify Developer Dashboard
2. Select your app
3. Add `http://localhost:3000/callback` to Redirect URIs
4. Save settings

### Issue: "CORS Error"
**Solution:** Ensure the backend server is running on `http://localhost:5000` and CORS middleware is configured correctly.

### Issue: "Playback Not Working"
**Solution:** 
- Ensure you have an active Spotify Premium account
- Check WebPlayback API permissions in your app settings
- Verify device is available for playback

### Issue: "No Audio Output"
**Solution:**
- Check browser volume settings
- Verify Spotify app isn't playing elsewhere
- Try refreshing the page
- Switch to a different playback device

---

## 🚀 Deployment

### Deploy to Heroku
```bash
heroku create spotify-clone-app
git push heroku main
heroku config:set SPOTIFY_CLIENT_ID=your_id
heroku config:set SPOTIFY_CLIENT_SECRET=your_secret
```

### Deploy Frontend to Vercel
```bash
npm install -g vercel
vercel
```

### Deploy to Netlify
```bash
npm run build
netlify deploy --prod --dir=build
```

---

## 📝 API Response Examples

### Search Response
```json
{
  "tracks": {
    "items": [
      {
        "id": "11dFghVLq2DqRiRaP7Xn73",
        "name": "Autumn Leaves",
        "artists": [{"name": "Bill Evans"}],
        "album": {"name": "Peace Piece", "images": [{"url": "..."}]},
        "duration_ms": 268000,
        "preview_url": "..."
      }
    ]
  }
}
```

### Playlist Response
```json
{
  "id": "37i9dQZF1DX0VUhbU3uGJP",
  "name": "Jazz Essentials",
  "tracks": {
    "total": 42,
    "items": [...]
  },
  "images": [{"url": "..."}]
}
```

### User Profile Response
```json
{
  "id": "userid123",
  "display_name": "John Doe",
  "email": "john@example.com",
  "followers": {"total": 50},
  "images": [{"url": "..."}]
}
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style
- Use ES6+ syntax
- Follow ESLint configuration
- Add comments for complex logic
- Keep components small and reusable

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [Spotify Web API Documentation](https://developer.spotify.com/documentation/web-api)
- [React Documentation](https://reactjs.org/docs)
- [Express.js Guide](https://expressjs.com/)
- [OAuth 2.0 Specification](https://oauth.net/2/)
- The open-source community for amazing tools and libraries

---

## 📞 Support & Contact

- 📧 Email: [Your Email]
- 🐙 GitHub: [@Aliwael12](https://github.com/Aliwael12)
- 💬 Issues: [GitHub Issues](https://github.com/Aliwael12/spotify-clone/issues)

---

## 🎯 Roadmap

- [ ] Mobile app version (React Native)
- [ ] Offline mode with service workers
- [ ] Collaborative playlists
- [ ] Social sharing features
- [ ] Advanced audio visualization
- [ ] Lyrics display integration
- [ ] Podcast support
- [ ] Social media integration
- [ ] Analytics dashboard
- [ ] Multi-language support

---

**Made with ❤️ by [Aliwael12](https://github.com/Aliwael12)**

*Last Updated: 2026-05-06*
