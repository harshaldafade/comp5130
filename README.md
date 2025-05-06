
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
# Add .env with CONNECTION_STRING
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
CONNECTION_STRING=mongodb://localhost:27017/shorturl
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

## 📸 Basic UI Screenshots


![0](https://github.com/user-attachments/assets/0d8fc363-9c31-4c43-b5b0-4a5ee6fc56c9)
![1](https://github.com/user-attachments/assets/822fc8ea-4e0e-4926-9f46-beb6d7a2dc48)


---

## 📄 License

MIT
