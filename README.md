
```markdown
# 🎬 Movidex – MERN Movie Watchlist App

**Movidex** is a full-stack MERN (MongoDB, Express, React, Node.js) application that allows users to register, log in, browse movies, and manage a personal watchlist. Each user's watchlist is private and securely protected using JWT authentication.

---

## 🚀 Features

- 🔐 **User Authentication**
  - Secure user registration and login
  - Passwords hashed using **bcrypt**
  - JWT-based route protection for secure APIs

- 🎥 **Movie Management**
  - Browse/search movies
  - Add or remove movies from a personal watchlist
  - Watchlist is **private and unique** to each user

- 💻 **Responsive UI**
  - Built with modern React
  - Fully responsive across devices

---

## 🗂️ Project Structure

```

movidex/             # React Frontend
│
├── public/
├── src/
│   ├── App.js
│   ├── styles.css
│   ├── components/
│   │   ├── Header.js
│   │   ├── Footer.js
│   │   ├── Moviefile/
│   │   │   ├── MoviesGrid.js
│   │   │   ├── MovieCard.js
│   │   │   ├── Watchlist.js
│   │   ├── Login/
│   │   │   ├── Loginpage.js
│   │   │   ├── Welcome.js
│   │   ├── Register/
│   │   │   ├── RegisterPage.js
│   │   │   ├── RegisterPage.css

movidex-api/         # Node.js + Express Backend
├── server.js
├── .env
├── models/
│   ├── Movies.js
│   ├── User.js
├── routes/
│   ├── moviesRoutes.js
│   ├── userRoutes.js
├── middleware/
│   └── auth.js

```

---

## 🧠 Architecture Diagram

```

\[ React Frontend ]
⇅ JWT
\[ Express API ]
⇅
\[ MongoDB Database ]

Frontend: UI, Authentication, Watchlist
Backend: API, JWT, Route Protection
Database: Movies & User Watchlists

````

---

## ⚙️ Setup & Run Locally

### 1. Backend Setup

```bash
cd movidex-api
npm install
````

Create a `.env` file in `movidex-api`:

```env
MONGO_URI=mongodb://localhost:27017/movie-plax
JWT_SECRET=your_jwt_secret
PORT=5000
```

Start MongoDB locally (e.g., using `mongod`), then run the backend:

```bash
npm start
```

### 2. Frontend Setup

```bash
cd movidex
npm install
npm start
```

Visit the app at: [http://localhost:3000](http://localhost:3000)

---

## 🔒 Security

* Passwords hashed with **bcrypt**
* JWT used for both authentication & authorization
* All protected routes validate the JWT token
* Each user’s watchlist is **isolated and secure**

---

## 🚀 Deployment

### Backend

* Deploy to [Render](https://render.com), [Heroku](https://heroku.com), or [Railway](https://railway.app)
* Set environment variables in deployment platform:

  * `MONGO_URI` (e.g., MongoDB Atlas)
  * `JWT_SECRET`
* Ensure HTTPS and proper CORS settings

### Frontend

* Deploy to [Vercel](https://vercel.com), [Netlify](https://www.netlify.com), or [Firebase Hosting](https://firebase.google.com/products/hosting)
* Set the API base URL to your deployed backend

### MongoDB

* Use [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) for a cloud-hosted database
* Whitelist backend server IP address for access

---

## 📝 Customization Ideas

* 🎬 Connect a real movie API (e.g., [TMDB](https://www.themoviedb.org/))
* ⭐ Add user ratings and genres
* 🗓️ Include movie release dates and summaries
* 🛡️ Add OAuth (Google/GitHub login)
* 📧 Email verification system

---

## 🙏 Credits

Built with ❤️ using the **MERN Stack**
Movie data is stored in MongoDB’s `movieslist` collection.

---

## 📧 Contact

For issues, questions, or contributions:
Open a GitHub issue or contact the maintainer directly.
Pull requests are always welcome!

```

