# 🐺 Andile Mathe — Portfolio

> Software Developer & AI Engineer, building full-stack web applications, backend systems, and AI agents.

🌐 **Live site (GitHub Pages):** [wolfceoo.github.io/Web-Devolpment-Journey](https://wolfceoo.github.io/Web-Devolpment-Journey)
🌐 **Mirror (self-hosted VPS):** add your domain here once DNS is pointed

---

## 👨‍💻 About Me

I'm a software developer with a National Diploma in Information Technology, working across full-stack web development, backend engineering, and AI agent systems (LangChain, LangGraph, RAG). I don't stop at the code — I set up and manage the infrastructure it runs on too (VPS, Nginx, SSL, Docker).

---

## 🛠️ Tech Stack

| Area | Technologies |
|---|---|
| Frontend | HTML, CSS, JavaScript, React |
| Backend | Node.js, Express.js, FastAPI, Flask, Django |
| AI & Automation | LangChain, LangGraph, RAG, n8n |
| Database | PostgreSQL, MySQL, MariaDB |
| DevOps | Docker, Nginx, GitHub Actions, VPS deployment |
| Networking | Network Engineering, Security Fundamentals |
| Tools | Git, GitHub, VS Code, Linux (Ubuntu/WSL) |

---

## 📁 Project Structure

```
Web-Devolpment-Journey/
├── index.html                       # Main site — Home, About, Portfolio, Services, Contact
├── styles.css                       # Stylesheet (responsive, mobile-first)
├── Andile.png                       # Profile image
├── Andile_Mathe_CV.pdf              # Downloadable CV (linked from the Home section)
├── deploy/
│   └── nginx.conf.example           # Reference Nginx config for VPS hosting
├── .github/workflows/
│   └── deploy-vps.yml               # Auto-deploys to the VPS on every push to main
└── README.md                        # You are here
```

---

## ✨ Features

- Responsive design — works on mobile, tablet and desktop
- Animated intro bars on page load
- Typewriter effect cycling through roles
- Rotating border profile image
- Full site sections: Home, About, Portfolio, Services, Contact
- Active nav-link highlighting on scroll
- Social links — GitHub, LinkedIn, Twitter
- Hamburger nav menu on mobile

---

## 🚀 Running Locally

```bash
# Clone the repo
git clone https://github.com/WolfCeoo/Web-Devolpment-Journey.git

# Navigate into it
cd Web-Devolpment-Journey

# Open in browser (no build step needed — pure HTML/CSS/JS)
open index.html
```

---

## 🌍 Deployment

This site is deployed to **two places** in parallel:

1. **GitHub Pages** — served automatically from the `main` branch. No action needed; it just works whenever you push.
2. **Self-hosted VPS** — mirrored via the `deploy-vps.yml` GitHub Action on every push to `main`.

### Setting up the VPS mirror

1. On your VPS, create a deploy directory (e.g. `/var/www/portfolio`) and set up Nginx using `deploy/nginx.conf.example` as a starting point.
2. Generate a dedicated SSH key pair for deployment (don't reuse your personal key):
   ```bash
   ssh-keygen -t ed25519 -f deploy_key -C "github-actions-deploy"
   ```
3. Add the **public** key to `~/.ssh/authorized_keys` on the VPS.
4. In the GitHub repo, go to **Settings → Secrets and variables → Actions** and add:
   - `VPS_HOST` — your VPS IP or domain
   - `VPS_USER` — the SSH user to deploy as
   - `VPS_SSH_KEY` — the **private** key contents (never commit this)
   - `VPS_PORT` — SSH port (usually `22`)
   - `VPS_DEPLOY_PATH` — the directory on the VPS to sync into (e.g. `/var/www/portfolio`)
5. Push to `main` — the workflow rsyncs the site to the VPS automatically. GitHub Pages keeps working independently the whole time.

---

## 📬 Connect

[![GitHub](https://img.shields.io/badge/GitHub-WolfCeoo-181717?style=flat&logo=github)](https://github.com/WolfCeoo)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Andile%20Mathe-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/andile-mathe)
[![Twitter](https://img.shields.io/badge/Twitter-@wolf__ceo-1DA1F2?style=flat&logo=twitter)](https://x.com/wolf__ceo)

---

*Built with HTML, CSS & JavaScript — no frameworks, no fluff.*
