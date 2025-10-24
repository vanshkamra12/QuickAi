# 🚀 QuickAI - Full-Stack AI Content Creation Platform

<div align="center">
  
  [![React](https://img.shields.io/badge/React-19.1.0-blue.svg)](https://reactjs.org/)
  [![Node.js](https://img.shields.io/badge/Node.js-Express-green.svg)](https://nodejs.org/)
  [![OpenAI](https://img.shields.io/badge/AI-Gemini%202.0-orange.svg)](https://ai.google.dev/)
  [![Cloudinary](https://img.shields.io/badge/Images-Cloudinary-blue.svg)](https://cloudinary.com/)
  [![Clerk](https://img.shields.io/badge/Auth-Clerk-purple.svg)](https://clerk.dev/)
</div>

## 📖 About

QuickAI is a comprehensive full-stack web application that harnesses the power of artificial intelligence to streamline content creation, image processing, and professional document review. Built with modern technologies, it offers a suite of AI-powered tools designed to boost productivity and creativity for content creators, marketers, and professionals.

## ✨ Features

### 🤖 AI-Powered Content Creation
- **AI Article Writer**: Generate high-quality, engaging articles on any topic using advanced AI
- **Blog Title Generator**: Create catchy, SEO-friendly blog titles for any category
- **Smart Content Dashboard**: Manage and track all your AI-generated content

### 🎨 Advanced Image Processing
- **AI Image Generation**: Create stunning visuals from text descriptions
- **Background Removal**: Effortlessly remove backgrounds from images with precision
- **Object Removal**: Seamlessly remove unwanted objects from photos
- **Cloudinary Integration**: Reliable image storage and optimization

### 📄 Professional Tools
- **Resume Reviewer**: Get AI-powered feedback to improve your resume
- **PDF Processing**: Upload and analyze PDF documents for review

### 👥 User Experience
- **Authentication**: Secure user authentication powered by Clerk
- **Responsive Design**: Beautiful, mobile-first design with Tailwind CSS
- **Real-time Notifications**: Toast notifications for user feedback
- **Community Features**: Connect with other users and share creations

### 💳 Subscription Management
- **Freemium Model**: 10 free AI generations for new users
- **Premium Plans**: Unlimited access with Clerk's pricing tables
- **Usage Tracking**: Monitor your AI tool usage

## 🛠️ Tech Stack

### Frontend
- **React 19.1.0** - Modern UI library
- **Vite** - Fast build tool and development server
- **React Router Dom** - Client-side routing
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide React** - Beautiful icon library
- **React Hot Toast** - Elegant notifications
- **React Markdown** - Markdown rendering
- **Axios** - HTTP client for API calls

### Backend
- **Node.js & Express** - Server runtime and framework
- **OpenAI API** (Gemini 2.0) - AI content generation
- **Cloudinary** - Image storage and processing
- **Neon Database** - PostgreSQL database
- **Clerk Express** - Authentication middleware
- **Multer** - File upload handling
- **PDF Parse** - PDF document processing

### Authentication & Security
- **Clerk** - Complete authentication solution
- **JWT Tokens** - Secure API authentication
- **CORS** - Cross-origin resource sharing

### Deployment
- **Vercel** - Hosting platform for both frontend and backend
- **Environment Variables** - Secure configuration management

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Clerk account
- OpenAI/Gemini API key
- Cloudinary account
- Neon Database account

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/quickai-full-stack.git
   cd quickai-full-stack
   ```

2. **Install dependencies for both client and server**
   ```bash
   # Install client dependencies
   cd client
   npm install
   
   # Install server dependencies
   cd ../server
   npm install
   ```

3. **Environment Setup**

   **Client (.env)**
   ```env
   VITE_BASE_URL=http://localhost:3000
   VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   ```

   **Server (.env)**
   ```env
   PORT=3000
   CLERK_SECRET_KEY=your_clerk_secret_key
   GEMINI_API_KEY=your_gemini_api_key
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   DATABASE_URL=your_neon_database_url
   ```

4. **Database Setup**
   ```sql
   CREATE TABLE creations (
     id SERIAL PRIMARY KEY,
     user_id VARCHAR(255) NOT NULL,
     prompt TEXT NOT NULL,
     content TEXT NOT NULL,
     type VARCHAR(50) NOT NULL,
     publish BOOLEAN DEFAULT FALSE,
     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
   ```

5. **Run the application**
   ```bash
   # Start the server (in server directory)
   npm run server
   
   # Start the client (in client directory)
   npm run dev
   ```

## 📁 Project Structure

```
QuickAI-Full-Stack/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Page components
│   │   ├── assets/         # Images and static files
│   │   └── App.jsx         # Main app component
│   ├── public/             # Public assets
│   └── package.json
├── server/                 # Express backend
│   ├── configs/            # Configuration files
│   ├── controllers/        # Request handlers
│   ├── middlewares/        # Custom middleware
│   ├── routes/             # API routes
│   └── server.js           # Entry point
└── README.md
```

## 🔗 API Endpoints

### AI Tools
- `POST /api/ai/article` - Generate AI articles
- `POST /api/ai/blog-title` - Generate blog titles
- `POST /api/ai/generate-image` - Create AI images
- `POST /api/ai/remove-background` - Remove image backgrounds
- `POST /api/ai/remove-object` - Remove objects from images
- `POST /api/ai/resume-review` - Review resume documents

### User Management
- `GET /api/user/get-user-creations` - Fetch user's creations
- `POST /api/user/update-creation` - Update creation visibility

## 🎯 Key Features Explained

### AI Article Writer
- Generates comprehensive articles based on user prompts
- Customizable length and tone
- Supports various topics and industries

### Blog Title Generator
- Creates multiple title suggestions
- Category-specific optimization
- SEO-friendly suggestions

### Image Processing Tools
- **Generation**: Text-to-image AI creation
- **Background Removal**: Automatic background detection and removal
- **Object Removal**: Intelligent object detection and seamless removal

### Resume Reviewer
- PDF upload and parsing
- AI-powered analysis and feedback
- Improvement suggestions

## 🔒 Authentication Flow
1. Users sign up/login via Clerk
2. JWT tokens secure API endpoints
3. User metadata tracks subscription plans
4. Free users limited to 10 generations
5. Premium users get unlimited access

## 🌟 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- [OpenAI/Google Gemini](https://ai.google.dev/) for AI capabilities
- [Clerk](https://clerk.dev/) for authentication
- [Cloudinary](https://cloudinary.com/) for image processing
- [Neon](https://neon.tech/) for database hosting
- [Vercel](https://vercel.com/) for deployment

---

