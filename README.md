# PAGASA Guimba Youth Organization Management Information System (MIS)

A modern, responsive Municipal Youth Information System & Digital Portal for **Pag-asa Youth Association of the Philippines - Guimba Chapter (PAGASA-Guimba)**.

---

## 🚀 Deployment Guide

### Option 1: Export to GitHub from AI Studio

1. In **Google AI Studio**, click the **Export** / **Settings** button in the top navigation bar.
2. Select **Export to GitHub** (or download the full repository as a **ZIP** archive).
3. Connect your GitHub account and create a new repository (e.g., `pagasa-guimba-youth-mis`).
4. AI Studio will automatically push all source code, dependencies, and configuration files to your new GitHub repository.

---

### Option 2: Deploy to Render (Web Service)

Render allows you to host the application for free with automatic SSL and continuous deployment from GitHub:

1. Sign up or log in at **[render.com](https://render.com/)**.
2. Click **New +** → **Web Service**.
3. Select **Build and deploy from a Git repository** and connect your GitHub repository `pagasa-guimba-youth-mis`.
4. Configure the service settings:
   - **Name**: `pagasa-guimba-mis` (or your preferred name)
   - **Language**: `Node`
   - **Branch**: `main`
   - **Build Command**: `npm install && npm run build`
   - **Start Command**: `npm start`
5. *(Optional)* Add Environment Variables in the **Environment** section:
   - `NODE_ENV`: `production`
   - `GEMINI_API_KEY`: *(Your Google AI Studio Gemini API key if using AI features)*
6. Click **Create Web Service**.
7. Render will build the Vite client and Node server bundle and deploy your application to a live public `.onrender.com` URL.

---

### Option 3: Deploy to Render as a Blueprint (Automatic)

Since this repository includes `render.yaml`:
1. In Render, select **New +** → **Blueprint**.
2. Connect your repository. Render will automatically read the build and start commands from `render.yaml` and configure everything for you.

---

## 💻 Local Development

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Start production server
npm start
```
