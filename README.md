# 🎵 Spotify Clone

A full-stack web application that replicates Spotify's core functionality with real music playback integration using Spotify's official APIs.


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
