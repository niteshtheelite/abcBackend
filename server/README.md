# 🚀 Backend API with Docker + Neon PostgreSQL

This project is a backend API containerized with Docker and connected to a cloud-hosted PostgreSQL database via [Neon](https://neon.tech). It's set up for easy local development and team collaboration.

---

## 🧑‍🤝‍🧑 How Your Teammates Can Set It Up Locally

Follow these steps to run the backend project on your local machine.

---

## 📦 Requirements

- [Docker](https://www.docker.com/products/docker-desktop) installed and running
- [Neon PostgreSQL account](https://neon.tech/) (project creator will share credentials)
- A code editor (e.g., [VS Code](https://code.visualstudio.com/))

---

## 🛠️ Step-by-Step Setup

### 1. Clone the Repository

```bash
git clone git@github.com:niteshtheelite/abcBackend.git
cd your-repo-name
```

---

### 2. Create Environment File

Copy the example environment file:

```bash
cp .env.example .env
```

Fill in the required values inside `.env` (ask your teammate or refer to Neon dashboard):

```env
PORT=5000
NODE_ENV=development
DATABASE_URL=postgresql://your-username:your-password@your-neon-host/dbname?sslmode=require
```

---

### 3. Start the Project Using Docker

Run the following command in the project directory:

```bash
docker-compose up --build
```

- This builds and starts the backend container.
- The app will be available at `http://localhost:5000` (or whatever port you set).

---

## 📁 Project Structure

```
project-root/
│
├── Dockerfile
├── docker-compose.yml
├── .env
├── .env.example
├── README.md
├── package.json
└── index.js (or your main server file)
```

---

## 🐳 Docker Tips

```bash
# Start normally
docker-compose up

# Rebuild the image and start
docker-compose up --build

# Stop the containers
docker-compose down

# View logs
docker-compose logs -f
```

---

## ❗ Important Notes

- Never commit the `.env` file — it's for your local secrets.
- Use `.env.example` to help teammates know what values are needed.
- You do **not** need a local database — Neon PostgreSQL runs in the cloud.

---

## ✅ You're Ready to Go!

Now you can start building and contributing to the backend API 🚀
