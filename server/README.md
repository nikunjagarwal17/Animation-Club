# 🚀 Animation Club Server

The backend that powers our Animation Club website. Handles user accounts, events, artwork submissions, and more.

## 🛠️ What's Inside

- **Node.js + Express** - The main server
- **MongoDB** - Where we store all the data
- **JWT** - Keeps user logins secure

## 📁 How It's Organized

```
server/
├── controllers/     # Handle different features (events, artworks, etc.)
├── models/         # Database schemas (what data looks like)
├── routes/         # API endpoints (where requests go)
├── middlewares/    # Security and validation
├── configs/        # Database and service connections
├── scripts/        # Helper tools for setup
└── server.js       # Main entry point
```

## 🚀 Getting Started

### Setup

1. **Install dependencies:**
```bash
npm install
```

2. **Create your `.env` file:**
```env
MONGODB_URI=your-mongodb-connection
JWT_SECRET=your-secret-key
PORT=5000
CLIENT_URL=http://localhost:4000
NODE_ENV=development #production
SESSION_TIMEOUT=30
MAX_LOGIN_ATTEMPTS=5
PASSWORD_MIN_LENGTH=6
AUTH_RATE_LIMIT_WINDOW_MS=900000         # 15 minutes
AUTH_RATE_LIMIT_MAX=20                  # 20 auth attempts per 15 minutes
AUTH_RATE_LIMIT_MESSAGE=Too many authentication attempts, please try again later.
API_RATE_LIMIT_WINDOW_MS=60000          # 1 minute
API_RATE_LIMIT_MAX=50                   # 100 API calls per minute
API_RATE_LIMIT_MESSAGE=API rate limit exceeded, please try again later.
```

3. **Run the server:**
```bash
npm run dev     # Development mode
npm start       # Production mode
```

## 🔒 Security & Features

- **Password protection** with hashing
- **JWT tokens** for secure login sessions
- **Rate limiting** to prevent spam
- **Input validation** on all data
- **Role-based access** (user vs admin vs manager)

## 🗃️ What We Store

### User Data
- Basic info (name, email, encrypted password)
- Profile details (bio, skills, year, department)
- Artwork submissions and event registrations

### Event Data  
- Event details (title, date, venue)
- Registration lists and event status

### Artwork Data
- Image URLs, titles, descriptions, categories
- Artist information and approval status
- View counts and featured status

### Achievement Data
- Club accomplishments with photos
- Awards, partnerships, and recognition details

### Opportunities Data
- Opportunities provied by the club reach
- Details and status for the opportunity