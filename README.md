# StreetArt

StreetArt is a web application that allows users to view, upload, and manage artwork and events related to street art. The application includes a map to display artwork locations, user authentication, and the ability to upload and view photos and events.

## Features

- **View Artwork**: Browse through uploaded artworks on a map.
- **User Authentication**: Sign up, sign in, and manage your profile.
- **Upload Artwork**: Upload photos of artwork with location, title, author, and description.
- **View Events**: Browse events on a calendar.
- **Manage Events**: Add new events and view event details.
- **Responsive Design**: Optimized for both desktop and mobile devices.

## Installation

### Prerequisites

- Node.js
- npm (Node Package Manager)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/streetart.git
   ```
2. Navigate to the project directory:
   ```bash
   cd streetart
   ```
3. Install the dependencies:
   ```bash
   npm install
   ```
4. Start the server:
   ```bash
   npm start
   ```
5. Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

## API Endpoints

### GET /

- **Description**: Home page displaying all artworks.
- **Response**: Renders the home page with artwork photos.

### GET /about

- **Description**: About page.
- **Response**: Renders the about page.

### GET /artwork

- **Description**: View all users and their uploaded artworks.
- **Response**: Renders the artwork page.

### GET /calendar

- **Description**: View events in a calendar.
- **Response**: Renders the calendar page.

### GET /users/:username

- **Description**: View user profile.
- **Params**: `username` - The username of the user.
- **Response**: Renders the user's profile page.

### GET /map

- **Description**: View artworks on a map.
- **Response**: Renders the map page.

### GET /api/artwork

- **Description**: Fetch all artwork data.
- **Response**: JSON array of artworks.

### GET /signin

- **Description**: Sign in page.
- **Response**: Renders the sign-in page.

### GET /signup

- **Description**: Sign up page.
- **Response**: Renders the sign-up page.

### POST /signup

- **Description**: Handle sign-up form submission.
- **Body**: `firstName`, `lastName`, `username`, `location`, `link`, `email`, `password`, `description`, `profilePicture`.
- **Response**: Redirects to the dashboard.

### POST /signin

- **Description**: Handle sign-in form submission.
- **Body**: `username`, `password`.
- **Response**: Redirects to the dashboard.

### GET /dashboard

- **Description**: User dashboard.
- **Response**: Renders the dashboard page with user data.

### POST /uploadPhoto

- **Description**: Upload a photo of artwork.
- **Body**: `title`, `author`, `location`, `description`, `photo`.
- **Response**: Redirects to the dashboard.

### POST /deletePhoto/:id

- **Description**: Delete a photo of artwork.
- **Params**: `id` - The ID of the photo.
- **Response**: Redirects to the dashboard.

### POST /signout

- **Description**: Sign out the user.
- **Response**: Redirects to the sign-in page.

### POST /add-event

- **Description**: Add a new event.
- **Body**: `title`, `host`, `date`, `location`, `yourName`, `yourEmail`, `eventUrl`, `description`, `photo`.
- **Response**: Redirects to the calendar.

### GET /event/:id

- **Description**: View event details.
- **Params**: `id` - The ID of the event.
- **Response**: Renders the event detail page.

### GET /description/:username/:filename

- **Description**: View artwork description.
- **Params**: `username` - The username of the uploader.
- **Params**: `filename` - The filename of the artwork.
- **Response**: Renders the artwork description page.

## File Structure

```
├── public/               # Static files
├── uploads/              # Uploaded files
├── views/                # EJS templates
├── data.json             # Data storage
├── users.json            # Users data storage
├── artwork.json          # Artwork data storage
├── events.json           # Events data storage
├── app.js                # Express application
└── README.md             # Readme file
```

## Dependencies

- express
- ejs
- multer
- path
- fs
- node-fetch
- body-parser
- bcrypt
- express-session
- node-schedule

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This README provides an overview of the project, installation instructions, API endpoints, file structure, and dependencies. Adjust any paths, repository URLs, or descriptions as needed to fit your specific project details.
