# Connectify — Connect, Share & Stay in Touch

A social networking web application built to make online interactions simple, engaging, and accessible. Connectify brings posts, conversations, and community activity together in one place, allowing users to share moments, discover people, and stay updated in real time.

## About the Project

Connectify is designed around the idea of making digital connections feel effortless. Users can create and manage posts, share media, interact with other people's content, and communicate through real-time messaging.

The application combines a React-based interface with a Node.js and Express backend, MongoDB for data management, and Socket.io for live communication. Authentication and cloud-based media storage help support a more secure and convenient social networking experience.

## What You Can Do

### 📝 Share Your Moments
- Publish posts containing text, images, and videos.
- Create, view, edit, and delete your own posts.
- Keep your content organized in one place.

### 💬 Chat in Real Time
- Communicate with other users through live messaging.
- Use Socket.io to support instant communication without repeatedly refreshing the page.

### ❤️ Interact With the Community
- Like and comment on posts.
- Follow people and build your social network.
- Explore user profiles and stay connected with friends.

### 🔔 Stay Updated
- Receive activity notifications for supported interactions.
- Keep up with relevant content through a personalized feed.

### 🔗 Share Content Anywhere
Share interesting posts with others through supported platforms such as WhatsApp, LinkedIn, Telegram, and X.

### 🔐 Authentication & Account Security
- JWT-based authentication for protected access.
- OTP-based verification for supported login flows.
- Google sign-in integration.
- Backend routes designed to restrict access to authorized users.

## Technology Behind Connectify

| Layer | Technologies |
|---|---|
| Frontend | React.js, Redux |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| Media Management | Cloudinary |
| Real-Time Features | Socket.io |
| Authentication | JWT, OTP, Google Authentication |
| Email Services | Nodemailer |
| UI Components | Material UI |

## Project Structure

The repository is organized into separate client and server applications.

```text
Connectify/
├── client/
│   ├── public/
│   ├── src/
│   ├── .env.local
│   └── package.json
│
├── server/
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── middleware/
│   ├── .env
│   └── package.json
│
└── README.md
```

*Note: The folder layout above is illustrative. Adjust it to match the actual files and folders in your repository.*

## Run Connectify Locally

Follow the steps below to set up the application on your computer.

### Prerequisites

Make sure you have installed:

- Node.js and npm
- Git
- A MongoDB database, either local or hosted on MongoDB Atlas
- A Cloudinary account for media uploads
- Credentials for any authentication and email services enabled in your implementation

### 1. Download the Repository

```bash
git clone <your-repository-url>
cd <your-project-folder>
```

Replace the placeholders with your actual GitHub repository URL and folder name.

### 2. Configure the Backend

Open the server directory:

```bash
cd server
npm install
```

Create a `.env` file inside `server` and configure the required values:

```env
MONGO_URI=your_mongodb_connection_string
PORT=3001
JWT_SECRET=your_private_jwt_secret

EMAIL=your_email_address
PASSWORD=your_email_app_password

CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

Use the exact variable names expected by your backend code. If your application uses separate credentials for Google authentication or OTP delivery, configure those as well.

Start the backend:

```bash
npm start
```

Keep this terminal running.

### 3. Configure the Frontend

Open another terminal from the project root:

```bash
cd client
npm install
```

Create a `.env.local` file inside `client`:

```env
REACT_APP_BACKEND_URL=http://localhost:3001
REACT_APP_CLOUDINARY_API_KEY=your_cloudinary_api_key
```

Check your frontend code for the environment variable names it actually uses. The `REACT_APP_` prefix is appropriate for Create React App; Vite projects generally use `VITE_` instead.

Start the frontend:

```bash
npm start
```

If your project uses Vite, use `npm run dev` instead.

Open the local URL displayed in the frontend terminal. The frontend and backend may run on different ports.

## Configuration & Security

Keep your credentials private while developing and deploying Connectify.

- Never commit `.env` or `.env.local` files containing real credentials.
- Add secret files to `.gitignore`.
- Use a strong, private JWT secret.
- Store email app passwords and Cloudinary secrets only in the appropriate environment.
- Validate incoming requests and protect private API routes on the backend.
- Keep frontend configuration limited to values intended to be public; never expose private API secrets in browser code.

## Contributing

Connectify can grow through small, focused improvements. If you want to contribute:

1. Fork the repository.
2. Create a branch for your change.
3. Implement and test the feature.
4. Commit your work with a meaningful message.
5. Push the branch to your fork.
6. Open a pull request describing the change.

Example:

```bash
git checkout -b feature/profile-improvements
git add .
git commit -m "Improve user profile experience"
git push origin feature/profile-improvements
```

## Future Improvements

Possible areas for further development include:

- More granular notification preferences.
- Improved feed ranking and content discovery.
- Enhanced profile customization.
- Additional privacy and account-management controls.
- More comprehensive automated testing and performance improvements.

These are potential enhancements, not a claim that they are already implemented.


## Acknowledgements

Connectify is built with the help of the open-source ecosystem, including React, Redux, Node.js, Express, MongoDB, Socket.io, Cloudinary, Material UI, and Nodemailer.

Thanks to the developers and communities who maintain these tools and make modern web application development possible.
