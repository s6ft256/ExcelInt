# Deployment Guide

## Quick Deployment Options

### 1. GitHub Pages (Recommended)
1. Push your code to a GitHub repository
2. Enable GitHub Pages in repository settings
3. The included workflow will automatically build and deploy

### 2. Static Hosting Services
Upload the built files to any of these services:
- **Netlify**: Drag and drop the `dist` folder after running `npm run build`
- **Vercel**: Connect your GitHub repository for automatic deployments
- **Firebase Hosting**: Use `firebase deploy` after configuring Firebase CLI

### 3. Direct File Hosting
For simple deployment, you can:
1. Upload just the `index.html` file to any web server
2. The application will work as a standalone file

## Build Commands

```bash
# Development
npm run dev        # Start development server at http://localhost:5173

# Production
npm run build      # Build optimized files to dist/ folder
npm run preview    # Preview the production build locally
```

## Configuration

Before deployment, ensure you:
1. Replace the Firebase configuration in `index.html` with your project's config
2. Configure Firestore security rules for production use
3. Test the application with your own Firebase project

## Security Notes

- The current Firebase configuration is for testing only
- Set up proper Firestore security rules before production deployment
- Consider implementing user authentication for production use