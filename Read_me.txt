Based on an analysis of your repository structure, code, and configuration files, here is the detailed breakdown of your Wanderlust project:

Project Name: Wanderlust

Project Description: A comprehensive full-stack web application for discovering, listing, and reviewing tourist destinations and accommodations (similar to Airbnb). Users can browse through various property listings, read and leave reviews, and if authenticated, create and manage their own property listings.

Frontend Technologies:

HTML5 & CSS3
JavaScript (Vanilla)
EJS (Embedded JavaScript): Used as the primary templating engine alongside ejs-mate for boilerplate layouts (Navbar, Footer, Flash messages).
Bootstrap 5 (v5.3.6): For responsive design, grids, and pre-built UI components.
FontAwesome: For styling icons.
Google Fonts: Utilizing the "Plus Jakarta Sans" typography.
Backend Technologies:

Node.js (Runtime Environment)
Express.js (Backend Web Framework)
MVC Architecture: Code is cleanly separated into Models, Views, and Controllers.
Database (on Render):

MongoDB Atlas: Hosted cloud database.
Mongoose ODM: Used for object data modeling and schema definitions.
Connect-Mongo: Used to store and persist user sessions securely in the MongoDB database, preventing session loss on server restarts.
Authentication:

Passport.js: Utilized alongside passport-local for robust local authentication (Username/Password).
passport-local-mongoose: Streamlines user schema setup and password hashing/salting.
express-session: Manages the active state of logged-in users via encrypted HTTP-only cookies.
Major Features Built:

User Authentication & Authorization: Secure signup, login, and logout. Middleware to restrict specific actions to authorized users (e.g., only the listing owner can edit/delete a listing).
Listing Management (CRUD): Users can Create, Read, Update, and Delete destination listings, complete with pricing, location, descriptions, and dynamic tax calculation features.
Review & Rating System: Logged-in users can leave 1-5 star ratings and comments on properties. Only the author of a review can delete it.
Cloud Image Uploads: Integration with Cloudinary (using multer and multer-storage-cloudinary) to allow users to seamlessly upload listing images, ensuring files are saved securely in the cloud rather than local ephemeral storage.
Flash Notifications: Real-time feedback alerts (e.g., "Successfully added a new listing!", "You must be logged in!") using connect-flash.
Server-Side Validation: Form data validation handled dynamically in the backend using the Joi library to prevent bad data from reaching the database.
REST APIs Developed:

Listings Routes:
GET /listings - Fetch all listings
POST /listings - Create a new listing
GET /listings/:id - Fetch specific listing details
PUT /listings/:id - Update a listing
DELETE /listings/:id - Delete a listing
Review Routes:
POST /listings/:id/reviews - Add a review to a listing
DELETE /listings/:id/reviews/:reviewId - Remove a review
User Routes:
GET / POST /signup - Register a new user
GET / POST /login - Authenticate an existing user
GET /logout - Terminate user session
Deployment:

Application server deployed on Render.
Database hosted on MongoDB Atlas.
Static image assets hosted on Cloudinary.
Challenges Solved:

Session Redirect Management: Implemented logic (saveRedirectUrl middleware) so that if an unauthenticated user tries to perform a protected action (like creating a listing), they are prompted to log in and automatically redirected back to their intended destination post-login.
Cloud Storage Integration: Overcame the ephemeral file storage limitations of free cloud hosting platforms (like Render) by routing image uploads via Multer directly to Cloudinary.
Data Integrity & Security: Built robust backend authorization checks (isOwner, isReviewAuthor) to guarantee that endpoints cannot be exploited to modify or delete data belonging to other users.
Asynchronous Error Handling: Utilized a centralized error wrapper (wrapAsync & ExpressError) to cleanly catch and handle server errors and Mongoose validation errors without crashing the app.
Additional Contributions:

Architected the application using standard MVC design patterns making the codebase highly maintainable.
Structured reusable UI components (navbar.ejs, footer.ejs, flash.ejs) using ejs-mate to prevent code duplication across the frontend.
