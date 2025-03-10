# PlaylistXchange

PlaylistXchange is a web application that allows users to seamlessly convert and transfer their playlists between different streaming platforms like Spotify and Apple Music. With easy authentication and an intelligent matching algorithm, users can recreate their favorite playlists on their preferred service with minimal effort.

# Key Features

- **Cross-Platform Playlist Conversion**: Convert and sync playlists between Spotify and Apple Music.
- **OAuth Authentication**: Secure login with Spotify and Apple Music accounts.
- **Smart Track Matching**: Automatically finds equivalent songs across platforms.
- **User Dashboard**: Manage, view, and edit converted playlists.
- **Fast & Reliable Backend**: Built with Spring Boot for high performance.
- **Modern Frontend**: Developed with React for a smooth user experience.
- **Database Storage**: PostgreSQL for storing user data and conversion history.
- **Secure API Communication**: OAuth and JWT-based authentication.

# Project Structure

<pre>
📂 playlist-xchange
├── 📂 backend (Spring Boot API)
│   ├── 📂 src/main/java/com/playlistxchange
│   │   ├── 📂 controllers (REST API endpoints)
│   │   │   ├── PlaylistController.java - API for playlist conversion
│   │   │   ├── AuthController.java - OAuth authentication with Spotify/Apple Music
│   │   ├── 📂 services (Business logic)
│   │   │   ├── PlaylistService.java - Handles playlist conversion logic
│   │   │   ├── SpotifyService.java - Integration with Spotify API
│   │   │   ├── AppleMusicService.java - Integration with Apple Music API
│   │   │   ├── MatchingService.java - Song matching algorithm
│   │   ├── 📂 repositories (Database access)
│   │   │   ├── PlaylistRepository.java - Playlist database operations
│   │   │   ├── UserRepository.java - User database operations
│   │   ├── 📂 models (Database entities)
│   │   │   ├── User.java - User model
│   │   │   ├── Playlist.java - Playlist model
│   │   │   ├── Track.java - Track model
│   │   ├── 📂 config (Configuration & Authentication)
│   │   │   ├── SecurityConfig.java - OAuth + JWT config
│   │   │   ├── AppConfig.java - General configurations
│   ├── 📂 resources
│   │   ├── application.yml - Application configuration (DB, API keys)
│   ├── pom.xml - Maven dependencies
│   ├── run_backend.sh - Script to run the backend
├── 📂 frontend (React App)
│   ├── 📂 src
│   │   ├── 📂 components
│   │   │   ├── PlaylistConverter.js - UI for playlist conversion
│   │   │   ├── Login.js - OAuth authentication
│   │   │   ├── Dashboard.js - Manage converted playlists
│   │   ├── 📂 api
│   │   │   ├── api.js - Handles API requests to the backend
│   │   ├── App.js - Main application page
│   │   ├── index.js - Entry point
│   ├── package.json - React dependencies
│   ├── run_frontend.sh - Script to run the frontend
├── 📂 database (PostgreSQL setup)
│   ├── schema.sql - Database schema definition
│   ├── migrations/ - Migration files
├── 📂 scripts (Deployment & Utilities)
│   ├── setup_db.sh - Database initialization script
│   ├── deploy.sh - Deployment script
├── 📂 tests (Unit & Integration tests)
│   ├── PlaylistServiceTest.java - Tests for playlist conversion
│   ├── MatchingServiceTest.java - Tests for song matching algorithm
│   ├── frontend-tests/ - React UI tests
├── docker-compose.yml - Docker configuration for PostgreSQL & backend
├── README.md - Project documentation
├── .env - Environment variables (API keys, DB config)
</pre>
