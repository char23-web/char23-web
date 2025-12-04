# Char23 Web Application

A modern web application with automated build and deployment pipeline.

## Features

- 🚀 Quick setup and development workflow
- 🔧 Automated CI/CD pipeline with GitHub Actions
- 📦 Modern dependency management with npm
- 🌐 Ready for deployment to GitHub Pages
- 💻 Local development server
- ⚙️ Environment configuration support

## Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (version 18 or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- Git

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/char23-web/char23-web.git
cd char23-web
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Start Development Server

```bash
npm start
```

This will start a local development server at `http://localhost:8080` and automatically open it in your browser.

## Available Scripts

### Development

- **`npm start`** - Start the development server on port 8080
- **`npm run dev`** - Alias for `npm start`

### Build & Test

- **`npm run build`** - Build the application for production
- **`npm test`** - Run tests

### Deployment

- **`npm run deploy`** - Prepare application for deployment

## Environment Configuration

1. Copy the example environment file:
   ```bash
   cp .env.example .env
   ```

2. Update `.env` with your configuration values as needed.

## Project Structure

```
char23-web/
├── .github/
│   └── workflows/
│       └── blank.yml       # CI/CD pipeline configuration
├── index.html              # Main HTML file
├── styles.css              # Stylesheet
├── app.js                  # Application JavaScript
├── package.json            # Dependencies and scripts
├── .env.example            # Environment configuration template
├── .gitignore             # Git ignore rules
└── README.md              # This file
```

## Deployment

### GitHub Pages

The application is configured to automatically deploy to GitHub Pages when changes are pushed to the `main` branch.

#### Setup GitHub Pages Deployment

1. Go to your repository settings
2. Navigate to "Pages" under "Code and automation"
3. Set the source to "gh-pages" branch
4. Save the changes

The CI/CD pipeline will automatically build and deploy your application on every push to `main`.

### Manual Deployment

For other deployment platforms:

1. Build the application:
   ```bash
   npm run build
   ```

2. Deploy the following files to your hosting provider:
   - `index.html`
   - `styles.css`
   - `app.js`

## CI/CD Pipeline

The project includes a GitHub Actions workflow that:

1. **Build and Test** (runs on every push and pull request)
   - Checks out the code
   - Sets up Node.js environment
   - Installs dependencies
   - Runs tests
   - Builds the application
   - Uploads build artifacts

2. **Deploy** (runs only on main branch)
   - Downloads build artifacts
   - Deploys to GitHub Pages

## Development Workflow

1. Create a new branch for your feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes and test locally:
   ```bash
   npm start
   ```

3. Commit your changes:
   ```bash
   git add .
   git commit -m "Description of your changes"
   ```

4. Push to GitHub:
   ```bash
   git push origin feature/your-feature-name
   ```

5. Create a Pull Request on GitHub

6. Once approved and merged, the application will automatically deploy

## Troubleshooting

### Port Already in Use

If port 8080 is already in use, you can specify a different port:

```bash
npx http-server . -p 3000
```

### Dependencies Installation Issues

Try clearing the npm cache and reinstalling:

```bash
rm -rf node_modules package-lock.json
npm cache clean --force
npm install
```

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the ISC License.

## Support

For questions or issues, please open an issue on GitHub.
