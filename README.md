# Artisan Frontend

A modern e-commerce platform built with Next.js and TypeScript.

## 🚀 Getting Started (For Beginners)

### Prerequisites
Before you begin, make sure you have these installed:
- [Node.js](https://nodejs.org/) (Download and install the LTS version)
- A code editor (like [Visual Studio Code](https://code.visualstudio.com/))

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd artisanfrontend
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Set Up Environment Variables
1. Create a new file named `.env.local` in the root directory
2. Copy and paste this content into the `.env.local` file:
```
NEXT_PUBLIC_API_URL=http://localhost:3001/api
```

### Step 4: Start the Development Server
```bash
npm run dev
```
The application will start on http://localhost:3000

## 📚 Project Structure

```
src/
├── app/           # Next.js app directory
├── components/    # Reusable UI components
├── lib/          # Utility functions and services
├── features/     # Feature-specific components
└── types/        # TypeScript type definitions
```

## 🔑 Authentication

The application uses JWT (JSON Web Tokens) for authentication. Here's how it works:

### Login Flow
1. User enters email and password
2. Frontend sends credentials to `/api/auth/login`
3. Backend validates credentials and returns a JWT token
4. Frontend stores the token in localStorage
5. Token is automatically included in all API requests

### Protected Routes
- Routes that require authentication are protected
- If no valid token is found, user is redirected to login
- Token is automatically refreshed when needed

## 🛍️ Features

### User Features
- User registration and login
- Product browsing and search
- Shopping cart management
- Order history

### Admin Features
- Product management
- Order management
- User management

## 🔧 Common Issues and Solutions

### API Connection Issues
- Make sure the backend server is running
- Check if the API URL in `.env.local` is correct
- Verify that CORS is properly configured

### Authentication Issues
- Clear localStorage and try logging in again
- Check if the token hasn't expired
- Verify that the backend is running

### Development Issues
- If you see TypeScript errors, run `npm run build` to check for type issues
- If styles aren't loading, make sure Tailwind CSS is properly configured
- If components aren't rendering, check the browser console for errors

## 📝 Testing the Application

### Manual Testing
1. Start both frontend and backend servers
2. Open http://localhost:3000 in your browser
3. Try registering a new user
4. Test the login functionality
5. Browse products and add them to cart
6. Test the checkout process

### Development Tools
- [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi) (Chrome Extension)
- [Redux DevTools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd) (Chrome Extension)

## 🛠️ Development

### Available Scripts
- `npm run dev`: Start development server
- `npm run build`: Build for production
- `npm start`: Start production server
- `npm run lint`: Run ESLint
- `npm run type-check`: Check TypeScript types

### Code Style
- Use TypeScript for all new files
- Follow the existing component structure
- Use Tailwind CSS for styling
- Write meaningful component and function names

## 📚 Learning Resources
- [Next.js Documentation](https://nextjs.org/docs)
- [React Documentation](https://reactjs.org/docs)
- [TypeScript Documentation](https://www.typescriptlang.org/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## 🔐 Security Notes
- Never commit the `.env.local` file
- Keep dependencies updated
- Use HTTPS in production
- Implement proper error handling

## 🎨 UI Components

The application uses a component-based architecture. Here are some key components:

### Authentication Components
- LoginForm
- RegisterForm
- AuthLayout

### Product Components
- ProductCard
- ProductList
- ProductDetail

### Cart Components
- CartItem
- CartSummary
- CheckoutForm

## 📱 Responsive Design

The application is fully responsive and works on:
- Desktop computers
- Tablets
- Mobile phones

## 🚀 Deployment

### Production Build
```bash
npm run build
npm start
```

### Environment Variables
Make sure to set these in your production environment:
- `NEXT_PUBLIC_API_URL`: Your production API URL
- `NEXT_PUBLIC_SITE_URL`: Your production site URL
