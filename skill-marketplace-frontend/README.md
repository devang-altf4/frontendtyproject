# Skill Marketplace Frontend

A modern React frontend application for a skill marketplace platform, built with Vite, React Router, and Tailwind CSS.

## Features

- ⚡ Built with Vite for fast development and optimized builds
- ⚛️ React 19 with modern hooks and components
- 🎨 Tailwind CSS for responsive design
- 🚀 React Router for client-side routing
- 🌙 Theme toggle functionality
- 📱 Responsive design for all devices
- 🔒 Authentication system integration
- 💫 Framer Motion animations

## Tech Stack

- **Frontend Framework**: React 19
- **Build Tool**: Vite
- **Styling**: Tailwind CSS v4
- **Routing**: React Router DOM
- **Authentication**: JWT integration
- **Real-time**: Socket.io client
- **Icons**: Lucide React
- **Animations**: Framer Motion

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd skill-marketplace-frontend
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env.local
```

4. Update the environment variables in `.env.local`:
```env
VITE_API_URL=http://localhost:5000
```

### Development

Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:3000`

### Building for Production

Create a production build:
```bash
npm run build
```

Preview the production build locally:
```bash
npm run preview
```

## Deployment to Vercel

This project is configured for easy deployment to Vercel:

### Option 1: Deploy via Vercel CLI

1. Install Vercel CLI:
```bash
npm install -g vercel
```

2. Login to Vercel:
```bash
vercel login
```

3. Deploy from your project directory:
```bash
vercel
```

4. Follow the prompts to configure your deployment

### Option 2: Deploy via Git Integration

1. Push your code to a Git repository (GitHub, GitLab, or Bitbucket)

2. Go to [vercel.com](https://vercel.com) and sign in

3. Click "New Project" and import your repository

4. Vercel will automatically detect the framework and configure the build settings

5. Set up environment variables in the Vercel dashboard:
   - Go to your project settings
   - Add environment variables:
     - `VITE_API_URL`: Your backend API URL
     - Add any other environment variables your app needs

6. Deploy!

### Environment Variables for Production

Make sure to set these environment variables in your Vercel dashboard:

- `VITE_API_URL`: Your production backend API URL
- Any other environment variables your app requires

### Build Configuration

The project includes optimized Vite configuration for production:

- **Output Directory**: `dist`
- **Code Splitting**: Automatic vendor and router chunks
- **Minification**: Terser for optimal bundle size
- **Source Maps**: Disabled in production for security

### Vercel Configuration

The `vercel.json` file is configured for:

- Static build deployment
- SPA routing (all routes redirect to `index.html`)
- Asset optimization
- Production environment settings

## Project Structure

```
src/
├── api/                 # API integration
├── assets/             # Static assets
├── components/         # Reusable UI components
├── pages/              # Page components
│   └── Auth/          # Authentication pages
├── router/            # Routing configuration
├── services/          # Business logic services
└── utils/             # Utility functions and helpers
    └── constants/     # Application constants
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run build:prod` - Build with production environment
- `npm run preview` - Preview production build locally
- `npm run serve` - Serve production build on port 3000
- `npm run lint` - Run ESLint
- `npm run clean` - Clean build directory

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and linting
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
