# Statstify - Spotify Statistics Viewer

A web application that provides personalized Spotify listening statistics using the Spotify Web API. View your top tracks, artists, and detailed audio features based on different time periods.

**Demo:** [YouTube](https://www.youtube.com/watch?v=xiUjepA6zVE)

## Features

- **OAuth Authentication** - Secure login through Spotify account
- **Top Tracks & Artists** - View your favorites across three time ranges (1 month, 6 months, 1 year)
- **Search Functionality** - Look up detailed stats for any track or artist
- **Audio Analysis** - View technical audio features (tempo, key, energy, etc.)

## Tech Stack

**Python** | **Flask** | **Spotify Web API** | **OAuth 2.0** | **HTML/CSS** | **JavaScript**

## Setup

1. Clone the repository
2. Create `.env` file with your Spotify API credentials:
```
CLIENT_ID=your_client_id
CLIENT_SECRET=your_client_secret
```
3. Install dependencies:
```bash
pip install flask requests python-dotenv
```
4. Run the application:
```bash
python app.py
```

## Project Structure
```
├── app.py              # Main Flask application
├── extra/              # Helper modules
│   ├── helpers.py      # Authentication & utility functions
│   ├── helpers2.py     # Data extraction functions
│   └── queries.py      # Spotify API calls
├── templates/          # HTML templates
├── static/             # CSS and JavaScript
└── .env                # API credentials (not committed)
```

## Usage

1. Visit the application and click "Login with Spotify"
2. Authorize Statstify to access your Spotify data
3. View your top tracks and artists on the homepage
4. Use search features to explore individual tracks and artists

## API Classes

- `userProfile()` - User information and profile picture
- `topTracks()` - User's most played tracks
- `topArtists()` - User's most listened artists
- `searchTracks()` - Search for specific tracks
- `searchArtists()` - Search for specific artists
- `trackStats()` - Detailed audio features
- `trackByID()` / `artistByID()` - Get details by ID
