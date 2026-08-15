# <img src="public/favicon.svg" alt="Wanderlust Logo" width="35" align="top"> Wanderlust

Wanderlust is a full-stack web application designed for booking and managing travel accommodations, heavily inspired by platforms like Airbnb. It allows users to browse listings, view destinations on a map, leave reviews, and even host their own properties.

The application features a **State-of-the-Art UI** with a premium glassmorphism design, vibrant gradients, and smooth micro-animations.

---

## ✨ Features

- **User Authentication:** Secure sign-up, log-in, and log-out functionality.
- **Property Listings:** View detailed information about properties, including pricing, location, and images.
- **Hosting:** Authenticated users can create, edit, and delete their own listings.
- **Reviews & Ratings:** Users can leave reviews and star ratings for properties they've visited.
- **Search & Filters:** Real-time search functionality and category filters (Trending, Iconic Cities, Mountains, etc.).
- **Tax Toggle:** Dynamically view prices with or without GST.
- **Premium UI:** Fully responsive design built with EJS, Vanilla CSS, and Bootstrap, featuring frosted glass (glassmorphism) navigation bars and animated listing cards.

---

## 🛠️ Tech Stack

**Frontend:**
- HTML / CSS / JavaScript
- EJS (Embedded JavaScript Templating)
- Bootstrap 5 (for grid and utilities)

**Backend:**
- Node.js
- Express.js (RESTful architecture)

**Database:**
- MongoDB (Atlas)
- Mongoose (ODM)

**Other Tools:**
- Cloudinary (Image hosting)
- Joi (Server-side data validation)
- Passport.js (Authentication)

---

## 📂 Project Structure

```text
Wanderlust/
├── controllers/       # Controller logic for MVC architecture
├── init/              # Database initialization and seeding scripts
├── models/            # Mongoose database schemas (User, Listing, Review)
├── public/            # Static assets (CSS, JS, Images, Favicon)
│   ├── css/           # Premium Vanilla CSS (style.css, rating.css)
│   └── js/            # Client-side JavaScript
├── routes/            # Express router files (listings, reviews, users)
├── utils/             # Utility functions and Error handling classes
├── views/             # EJS Templates
│   ├── includes/      # Partials (navbar, footer, flash messages)
│   ├── layouts/       # Main boilerplate layout
│   ├── listings/      # Listing specific pages (index, show, new, edit)
│   └── users/         # Authentication pages (login, signup)
├── .env               # Environment variables (ignored in Git)
├── AGENTS.md          # AI Assistant guidelines for the project
├── app.js             # Main application entry point
├── cloudConfig.js     # Cloudinary configuration
├── middleware.js      # Custom Express middlewares (auth, validation)
├── package.json       # Node.js dependencies
└── schema.js          # Joi validation schemas
```

---

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ASIM-XD/WanderLust_Travel_Accomodation_App.git
   cd wanderlust
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up Environment Variables:**
   Create a `.env` file in the root directory and add the following keys:
   ```env
   CLOUD_NAME=your_cloudinary_name
   CLOUD_API_KEY=your_cloudinary_api_key
   CLOUD_API_SECRET=your_cloudinary_api_secret
   ATLASDB_URL=your_mongodb_atlas_connection_string
   SECRET=your_express_session_secret
   ```

4. **Run the Application:**
   ```bash
   node app.js
   ```
   The server will start on `http://localhost:8080`.
