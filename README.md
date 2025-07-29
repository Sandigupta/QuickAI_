# AI SaaS Platform (PERN Stack)

A powerful, subscription-based **AI SaaS platform** that empowers users with AI-powered tools for content creation, image editing, and resume analysis. Designed using modern web technologies and cloud infrastructure, this application streamlines complex creative tasks into a seamless user experience.

---

## Real-World Problem & Solution

Content creators, marketers, designers, and job seekers frequently encounter time-consuming tasks such as writing articles, editing images, and analyzing resumes. This platform offers **AI-powered solutions** to automate and accelerate these workflows—saving time and boosting productivity.

Our app addresses:
- Tedious manual article and title generation
- Time-intensive image editing (object/background removal)
- Resume analysis for job seekers
- The need for a unified, subscription-based dashboard with scalable infrastructure

---

## Dashboard Preview

<img width="1920" height="4092" alt="Image" src="https://github.com/user-attachments/assets/dd4d92c2-956d-4654-920f-e283318b82a6" />

---

## 🧰 Tech Stack

| Technology               | Reason for Use                                                                 |
|--------------------------|--------------------------------------------------------------------------------|
| **React + Vite**         | Blazing-fast frontend tooling and developer-friendly environment               |
| **Tailwind CSS**         | Rapid UI development with responsive, utility-first styling                   |
| **Node.js + Express**    | Lightweight backend with scalable API support                                 |
| **PostgreSQL (Neon)**    | Serverless relational DB with automatic scaling and pooling                    |
| **Clerk**                | Plug-and-play authentication with secure session handling                     |
| **Cloudinary**           | Efficient media storage, transformation, and CDN delivery                     |
| **Multer**               | File upload middleware for handling images and PDFs                           |
| **OpenAI API**           | Language generation for articles, resumes, and ideation                       |
| **Gemini API**           | Advanced multimodal capabilities for image generation                         |
| **pdf-parse**            | Text extraction and structuring from uploaded resumes                         |
| **Axios**                | Streamlined HTTP requests from both frontend and backend                      |

---

## 🏗️ System Architecture

<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/2767596b-c703-4667-8d09-c31e416680c0" />

---

## 🔐 Environment Configuration

Add the following environment variables in a `.env` file:

```env
# AI API Keys
OPENAI_API_KEY=your_openai_key
GEMINI_API_KEY=your_gemini_key

# Authentication (Clerk)
CLERK_SECRET_KEY=your_clerk_secret
CLERK_PUBLISHABLE_KEY=your_clerk_publishable

# Database (Neon)
PGHOST=your_db_host
PGDATABASE=your_db_name
PGUSER=your_db_user
PGPASSWORD=your_db_password
PGPORT=5432

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_key
CLOUDINARY_API_SECRET=your_cloudinary_secret
```

---

## 📡 API Endpoints

### 🧠 AI Feature Routes

| Endpoint                     | Method | Auth | Description                                   |
|------------------------------|--------|------|-----------------------------------------------|
| `/api/ai/generate-article`   | POST   | ✅    | Generate AI-written article from title/length |
| `/api/ai/generate-blog-title`| POST   | ✅    | Generate blog titles from keywords/category   |
| `/api/ai/generate-image`     | POST   | ✅    | Generate image based on a prompt              |
| `/api/ai/remove-image-background` | POST | ✅  | Upload image and remove background            |
| `/api/ai/remove-image-object` | POST | ✅    | Remove specified object from uploaded image   |
| `/api/ai/resume-review`      | POST   | ✅    | Analyze uploaded resume and provide feedback  |
---
### 👤 User-Centric Routes

| Endpoint                     | Method | Auth | Description                              |
|------------------------------|--------|------|------------------------------------------|
| `/api/user/get-user-creations` | GET  | ✅    | Fetch all AI content by the user         |
| `/api/user/get-published-creations` | GET | ✅ | Fetch published content only             |
| `/api/user/toggle-like-creation` | POST | ✅ | Like/unlike specific AI content          |



## 🧪 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-org/ai-saas-platform.git
cd ai-saas-platform
```

### 2. Setup Backend

```bash
cd server
npm install
cp .env.example .env  # Fill in required secrets
npm run dev
```

### 3. Setup Frontend

```bash
cd client
npm install
cp .env.example .env  # Add Clerk keys and base API URL
npm run dev
```

---

## 🧼 Features

- **Secure Auth**: Session and identity handled via Clerk
- **Subscription System**: Upgrade to premium for full AI access
- **Cloudinary Uploads**: Secure image & file hosting
- **AI Integrations**: Uses both OpenAI and Gemini for various use cases
- **Responsive UI**: Built with Tailwind + Vite + Clerk components
- **Resume Parsing**: Built-in analysis for job applicants

---

## 🛡️ Security Notes

- All AI endpoints are protected with middleware-based authentication
- Rate limiting and input validation recommended for production
- Never expose `.env` keys in frontend or public repositories

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

