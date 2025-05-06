
# 🔗 URL Shortener

A full-stack URL shortener built with **React + TypeScript + Tailwind** on the frontend and **Node.js + Express + MongoDB** on the backend. Paste a long URL, get a short one. Click tracking included.

---

## 🚀 Tech Stack

### Frontend (`client-app/url-shortner-app`)
- React + TypeScript
- Tailwind CSS
- Vite

### Backend (`server-app`)
- Node.js + Express + TypeScript
- MongoDB + Mongoose
- NanoID (for short URL codes)

---

## 📁 Folder Structure

```
URL-SHORTNER/
├── client-app/
│   └── url-shortner-app/     # React app
│       ├── public/
│       ├── src/
│       │   ├── components/   # UI components
│       │   ├── helpers/      # Constants
│       │   └── interface/    # TypeScript types
├── server-app/               # Node/Express backend
│   ├── src/
│   │   ├── config/           # DB config
│   │   ├── controllers/      # Logic for shortening/redirect
│   │   ├── model/            # Mongoose schema
│   │   └── routes/           # API routes
```

---

## 🧪 API

### `POST /api/shorten`
Create a new short URL.
```json
{ "fullUrl": "https://example.com" }
```
➡️ Returns:
```json
{ "shortUrl": "abc123xyz0" }
```

### `GET /:shortUrl`
Redirects to the original URL. Increments click count.

---

## 🛠️ Setup

### Backend
```bash
cd server-app
npm install
# Add .env with MONGO_URI
npm run dev
```

### Frontend
```bash
cd client-app/url-shortner-app
npm install
npm run dev
```

---

## 🌱 .env Example

```env
MONGO_URI=mongodb://localhost:27017/shorturl
PORT=5000
BASE_URL=http://localhost:5000
```

---

## 📎 Example MongoDB Schema

```ts
fullUrl: String,
shortUrl: { type: String, default: () => nanoid().substring(0, 10) },
clicks: Number
```

---

## ✅ To-Do

- [ ] Add QR code support
- [ ] User accounts
- [ ] Analytics dashboard

---

## 📸 Screenshot Placeholder

*(Add a UI screenshot here)*

---

## 📄 License

MIT
