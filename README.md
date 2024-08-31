# AsanaMitra

Welcome to **AsanaMitra**, an AI-powered yoga platform designed to provide personalized yoga plans, interactive guided sessions, community features, and progress tracking. This platform aims to help users enhance their yoga practice through tailored experiences and community support.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Tech Stack](#tech-stack)
3. [Folder Structure](#folder-structure)
4. [Getting Started](#getting-started)
5. [Running the Application](#running-the-application)
6. [Contributing](#contributing)
7. [License](#license)

## Project Overview

AsanaMitra is a comprehensive yoga platform offering features such as:

- **Personalized Yoga Plans**: AI-generated plans based on user preferences and goals.
- **Interactive Guided Sessions**: Real-time feedback and guidance using AI and machine learning.
- **Community Features**: Engage with other users through forums and groups.
- **Progress Tracking**: Track your progress and achievements over time with visualizations and insights.

## Tech Stack

AsanaMitra utilizes a modern tech stack to provide a seamless user experience:

- **Front-End**: React.js, Redux, Tailwind CSS
- **Back-End**: Node.js, Express.js, MongoDB
- **AI/ML**: TensorFlow, OpenAI GPT-4, MediaPipe
- **DevOps**: Docker, Kubernetes, CI/CD with GitHub Actions
- **Cloud Services**: AWS/GCP for hosting and scaling

## Folder Structure

This folder structure is an initial setup based on the current requirements. It is designed to be scalable and modular, allowing for easy maintenance and expansion as the project grows.

# Folder Structure

## Project root structure

```plaintext
asana-mitra/
├── frontend/              # Front-end code
├── backend/               # Back-end code
├── ai-models/             # AI and ML models
├── shared/                # Shared utilities, types, and assets
├── docker/                # Docker configuration
├── scripts/               # Scripts for automation tasks
├── .env                   # Environment variables
├── .gitignore             # Git ignore file
├── README.md              # Project documentation
└── package.json           # Project dependencies and scripts
```

### Frontend

This folder contains all the front-end related code and assets, primarily built using React.js.

```plaintext
asana-mitra/frontend/
├── public/                      # Static files served directly
│   ├── index.html               # Main HTML file
│   └── assets/                  # Images, icons, fonts
├── src/                         # Source code
│   ├── components/              # Reusable UI components
│   │   ├── Header.jsx
│   │   ├── Footer.jsx
│   │   ├── YogaPlanCard.jsx
│   │   └── ...                  # Other components
│   ├── pages/                   # Page components
│   │   ├── Home.jsx
│   │   ├── Dashboard.jsx
│   │   ├── YogaPlans.jsx
│   │   ├── GuidedSession.jsx
│   │   ├── Community.jsx
│   │   ├── Profile.jsx
│   │   └── ...                  # Other pages
│   ├── context/                 # React Context for state management
│   │   ├── UserContext.jsx
│   │   └── YogaPlanContext.jsx
│   ├── hooks/                   # Custom React hooks
│   │   ├── useAuth.js
│   │   ├── useYogaPlans.js
│   │   └── ...                  # Other hooks
│   ├── services/                # API service functions
│   │   ├── authService.js
│   │   ├── yogaPlanService.js
│   │   └── ...                  # Other services
│   ├── styles/                  # Styling files (CSS, SCSS)
│   │   ├── globals.scss
│   │   ├── Home.module.scss
│   │   └── ...                  # Other style files
│   ├── App.jsx                  # Main App component
│   ├── index.jsx                # Entry point for React app
│   └── router.js                # React Router configuration
├── .env                         # Front-end specific environment variables
├── package.json                 # Front-end dependencies and scripts
└── webpack.config.js            # Webpack configuration (if using Webpack)
```

> **Note**: Before making any frontend modifications, make sure to install the Live Sass Compiler extension in VS Code and apply the following settings to your VS code `settings.json` file:

```plaintext
{
  "liveSassCompile.settings.generateMap": true,
  "liveSassCompile.settings.watchOnLaunch": true,
  "liveSassCompile.settings.formats": [
    {
      "format": "expanded",
      "extensionName": ".css",
      "savePath": "~/../css",
      "savePathReplacementPairs": null
    },
    {
      "format": "compressed",
      "extensionName": ".min.css",
      "savePath": "~/../min",
      "savePathReplacementPairs": null
    }
  ]
}
```

### Backend

This folder includes all back-end related code, using Node.js and Express.js for building APIs.

```plaintext
asana-mitra/backend/
├── config/                     # Configuration files
│   ├── db.js                   # Database connection configuration
│   ├── auth.js                 # Authentication settings
│   └── ...                     # Other configuration files
├── controllers/                # Controller functions for handling requests
│   ├── authController.js
│   ├── yogaPlanController.js
│   ├── sessionController.js
│   └── ...                     # Other controllers
├── models/                     # Mongoose models (for MongoDB)
│   ├── User.js
│   ├── YogaPlan.js
│   ├── Session.js
│   └── ...                     # Other models
├── routes/                     # API route definitions
│   ├── authRoutes.js
│   ├── yogaPlanRoutes.js
│   ├── sessionRoutes.js
│   └── ...                     # Other routes
├── middlewares/                # Middleware functions
│   ├── authMiddleware.js
│   ├── errorHandler.js
│   └── ...                     # Other middleware
├── utils/                      # Utility functions
│   ├── logger.js
│   ├── responseHandler.js
│   └── ...                     # Other utilities
├── tests/                      # Test files for back-end
│   ├── authController.test.js
│   ├── yogaPlanController.test.js
│   └── ...                     # Other tests
├── app.js                      # Express application setup
├── server.js                   # Entry point for server
├── .env                        # Server specific environment variables
├── package.json                # Back-end dependencies and scripts
└── Dockerfile                  # Docker configuration for the server
```

### Ai Models

This folder is dedicated to AI and machine learning models, handling tasks like natural language processing and pose detection.

```plaintext
asana-mitra/ai-models/
├── recommendation-engine/      # Models for generating personalized yoga plans
│   ├── train.py                # Training script
│   ├── model.py                # Model architecture
│   ├── utils.py                # Utility functions for data processing
│   └── ...                     # Other files
├── nlp/                        # NLP models for interactive guided sessions
│   ├── generate_session.py     # Script to generate session content
│   ├── nlp_model.py            # Model definition
│   └── ...                     # Other files
├── pose-detection/             # Models for real-time pose detection
│   ├── pose_estimator.py       # Pose detection logic
│   ├── utils.py                # Helper functions
│   └── ...                     # Other files
├── data/                       # Data used for training models
│   ├── yoga_poses.csv
│   ├── user_data.json
│   └── ...                     # Other datasets
├── requirements.txt            # Python dependencies for AI models
└── Dockerfile                  # Docker configuration for AI model deployment
```

### Shared

Contains shared resources that can be used across both client and server, like types, assets, and shared utilities.

```plaintext
asana-mitra/shared/
├── assets/                     # Shared assets like images, icons
│   ├── logo.png
│   └── ...
├── utils/                      # Shared utility functions
│   ├── validators.js           # Data validation functions
│   └── ...
├── types/                      # TypeScript types (if using TypeScript)
│   ├── user.d.ts
│   ├── yogaPlan.d.ts
│   └── ...
└── constants.js                # Shared constants
```

### Docker

Contains configuration files for containerizing and deploying the application.

```plaintext
asana-mitra/docker/
├── docker-compose.yml          # Docker Compose configuration for multi-container setup
├── client.Dockerfile           # Docker configuration for the client
└── server.Dockerfile           # Docker configuration for the server
```

### Scripts

Scripts for automation tasks such as database migration, data seeding, and deployment.

```plaintext
asana-mitra/scripts/
├── migrate.js                  # Script for database migrations
├── seed.js                     # Script to seed the database with initial data
└── deploy.sh                   # Script for deployment automation
```

### Root Level Files

Essential configuration and documentation files.

```plaintext
asana-mitra/
├── .env                        # Global environment variables
├── .gitignore                  # Specifies files to ignore in Git
├── README.md                   # Project documentation and instructions
├── package.json                # Dependencies for the entire project (monorepo approach)
└── yarn.lock / package-lock.json # Dependency lock files
```

## Running the Application

### Getting Started

To get started with AsanaMitra, follow these steps:

### 1. Clone the repository:

```bash
git clone https://github.com/yourusername/asana-mitra.git
cd asana-mitra
```

### 2. Install dependencies:

```bash
# Install front-end dependencies
cd frontend
yarn install

# Install back-end dependencies
cd ../backend
yarn install
```

### 3. Set up environment variables:

Create a '.env' file in the 'root', 'client', and 'server' directories with the necessary environment variables.

### 4. Running the Application:

```bash
# Start the front-end development server
cd frontend
yarn start

# Start the back-end server
cd ../backend
yarn dev
```

## Contributing

We welcome contributions to AsanaMitra! Please follow the guidelines below:

- Fork the repository and create a new branch for your feature or bug fix.
- Write clear and concise commit messages.
- Test your code thoroughly before submitting a pull request.
- Provide a detailed description of your changes in the pull request.

## License

This project is licensed under the [MIT License](LICENSE). See the [LICENSE](LICENSE) file for details.
