# 🎵 SoundVault — Premium Digital Music Marketplace

> A production-ready, full-stack digital marketplace for selling Music Sample Packs, Drum Kits, Loop Packs, MIDI Packs, Presets, Sound Effects, Templates, Video Courses, and Digital Downloads.

![SoundVault Banner](docs/banner.png)

## ✨ Features

- 🎨 **Premium Spotify-inspired Dark UI** with Glassmorphism, Framer Motion animations
- 🔐 **Admin-only login** — customers browse & buy without accounts
- 🛒 **Guest Checkout** — Stripe, Razorpay, PayPal, UPI, Apple/Google Pay
- 🎧 **Waveform Audio Player** — watermarked previews, DRM-protected downloads
- 📦 **Drag & Drop Uploads** — resumable, bulk, with progress tracking
- 🤖 **AI-powered Search** — genre, mood, BPM, key, instrument understanding
- 📜 **Multi-license system** — Personal, Commercial, Unlimited, Exclusive, Enterprise
- 💳 **Subscription Plans** — Starter → Enterprise with recurring billing
- 🔗 **Affiliate System** — referral links, commissions, payout management
- 🔒 **DRM Protection** — signed URLs, temp links, download limits, watermarks
- 📊 **Full Admin Dashboard** — sales, revenue, orders, analytics, SEO settings
- ⚡ **Next.js App Router** + TypeScript + Tailwind CSS + Prisma + PostgreSQL + Redis

---

## 🗂️ Project Structure

```
soundvault-marketplace/
├── apps/
│   └── web/                    # Next.js 14 App Router frontend + API
│       ├── app/                # App Router pages
│       │   ├── (shop)/         # Public storefront routes
│       │   ├── (admin)/        # Admin panel routes (auth-protected)
│       │   └── api/            # API route handlers
│       ├── components/         # Reusable UI components
│       ├── lib/                # Core utilities, services
│       ├── hooks/              # Custom React hooks
│       ├── store/              # Zustand global state
│       ├── styles/             # Global CSS
│       └── types/              # TypeScript types
├── packages/
│   ├── database/               # Prisma schema + migrations
│   ├── email/                  # Email templates (React Email)
│   └── config/                 # Shared config
├── infrastructure/
│   ├── docker/                 # Docker + docker-compose
│   └── nginx/                  # Nginx reverse proxy config
├── docs/                       # Documentation
└── scripts/                    # Seed, deploy, migration scripts
```

---

## 🚀 Quick Start

### Prerequisites

- Node.js 20+
- pnpm 9+
- PostgreSQL 16+
- Redis 7+
- Docker (optional)

### 1. Clone & Install

```bash
git clone https://github.com/poovarasantevar01-dot/soundvault-marketplace.git
cd soundvault-marketplace
pnpm install
```

### 2. Environment Setup

```bash
cp apps/web/.env.example apps/web/.env.local
# Fill in all required environment variables
```

### 3. Database Setup

```bash
pnpm db:generate
pnpm db:push
pnpm db:seed
```

### 4. Start Development

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000)

Admin panel: [http://localhost:3000/admin](http://localhost:3000/admin)

---

## 🐳 Docker Deployment

```bash
cd infrastructure/docker
docker-compose up -d
```

---

## 📖 Full Documentation

See [docs/](./docs/) for:
- [Architecture Overview](docs/architecture.md)
- [API Reference](docs/api.md)
- [Admin Guide](docs/admin-guide.md)
- [Deployment Guide](docs/deployment.md)
- [Environment Variables](docs/env-vars.md)

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Next.js 14, React 18, TypeScript |
| Styling | Tailwind CSS, Framer Motion |
| Backend | Next.js API Routes, Node.js |
| ORM | Prisma ORM |
| Database | PostgreSQL 16 |
| Cache | Redis (ioredis) |
| Auth | NextAuth.js (admin only) |
| Payments | Stripe, Razorpay, PayPal |
| Storage | Cloudflare R2 / AWS S3 |
| CDN | Cloudflare |
| Email | Resend + React Email |
| Search | Meilisearch |
| Audio | WaveSurfer.js |
| Video | Video.js + HLS.js |
| Uploads | Uppy + TUS Protocol |
| State | Zustand |
| Forms | React Hook Form + Zod |
| Admin UI | Tremor + shadcn/ui |
| Analytics | Plausible / PostHog |
| DRM | Custom signed URLs (Cloudflare/S3) |

---

## 📄 License

MIT License — see [LICENSE](LICENSE)
