# Flashcards Learning App

A modern flashcards learning application built with React Native (Expo) and Express, using Xata as the database and Cloudinary for image storage.

## Features

- Create and manage flashcard sets with titles, descriptions, and cover images
- Add cards to sets with questions and answers
- Study flashcards with learning sessions
- Track learning progress and scores
- User authentication using device storage
- Image uploads via Cloudinary
- Responsive UI for mobile devices

## Architecture

### Frontend (React Native/Expo)

The frontend is built with React Native using Expo, providing a cross-platform mobile experience. Key components:

- **Navigation**: Uses Expo Router for seamless navigation between screens
- **API Client**: Centralizes all API calls to the backend server
- **Screens**:
  - Home: Browse available flashcard sets
  - Create Set: Form to create new sets with image uploads
  - Cards: View and manage cards within a set
  - Learn: Interactive learning sessions
  - Profile: User profile and learning statistics

### Backend (Express)

The backend is built with Express.js and provides RESTful API endpoints:

- **Set Management**: Create, read, update, and delete flashcard sets
- **Card Management**: Create and retrieve cards within sets
- **User Learning**: Track user learning sessions and progress
- **Image Upload**: Handle image uploads using Cloudinary integration

### Data Storage

- **Xata**: Primary database for storing sets, cards, user data, and learning statistics
- **Cloudinary**: Cloud storage for images, providing optimized delivery and transformation

## Setup and Installation

### Prerequisites

- Node.js (v14 or later)
- npm or yarn
- Expo CLI
- Xata account
- Cloudinary account

### Environment Variables

Create a `.env` file in the api directory:

```
PORT=3000
XATA_API_KEY=your_xata_api_key
XATA_BRANCH=main
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

Create a `.env` file in the ankiApp directory:

```
EXPO_PUBLIC_API_URL=http://your-local-ip:3000
```

### Backend Setup

```bash
cd api
npm install
npm run dev
```

### Frontend Setup

```bash
cd ankiApp
npm install
npm run start
```

Then use Expo Go on your mobile device or an emulator to run the application.

## Usage

1. **Create a set**: Tap the "Create" button to create a new flashcard set
2. **Add cards**: Open a set and add cards with questions and answers
3. **Study**: Select a set and start a learning session
4. **Track progress**: View your learning statistics on the profile screen

## API Endpoints

- `GET /sets`: Get all sets
- `GET /sets/:id`: Get a specific set
- `POST /sets`: Create a new set
- `DELETE /sets/:id`: Delete a set
- `GET /usersets`: Get all sets for a user
- `POST /usersets`: Add a set to user favorites
- `GET /cards`: Get all cards for a set
- `POST /cards`: Create a new card
- `GET /cards/learn`: Get cards for learning
- `POST /learnings`: Save learning progress
- `GET /learnings`: Get user learning history
- `POST /upload`: Upload an image to Cloudinary

## Future Improvements

- User authentication with JWT
- Social sharing of sets
- Advanced statistics and learning algorithms
- Offline mode
- Web version

## Credits

This project was built as part of the nFactorial programming course.
