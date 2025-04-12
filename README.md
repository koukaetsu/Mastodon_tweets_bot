# 🐦 Tweets-to-Mastodon Bot (2022 Archive)

> ⚠️ This script is no longer in use. It was originally built in 2022 as an early project during my self-learning of Python automation, web scraping, and bot communication via API.  
> I'm keeping it here as a personal record of my development progress.

---

## 💡 Project Summary

This Python bot monitors specific Twitter users' activity, optionally translates the content, and automatically reposts it to a Mastodon account via direct messages.

🛠️ It was deployed and operated on **a self-hosted Mastodon instance**, running on **my own VPS with a custom domain**, fully set up using **Docker** and managed via **SSH remote connection**.

The bot simulated cross-platform "tweet forwarding" before Twitter API limitations and hosting costs led to the server shutdown.

---

## 🛠️ Features

- ✅ Uses [`Scweet`](https://github.com/Altimis/Scweet) to scrape tweets by user and time range
- 🌐 Optional content translation using `google_trans_new`
- 📤 Posts results as **direct messages (DM)** to users on Mastodon
- 📥 Recognizes commands via content pattern matching in `on_update`
- 🔁 Supports translation mode (`Y/N`) and multiple forwarding options

---

## 🖥️ Deployment Details

- **Hosting**: Cloud VPS server (Debian/Linux), self-managed
- **Containerization**: Entire Mastodon instance was deployed using Docker Compose  
  (Redis, PostgreSQL, Sidekiq, Mastodon services in containers)
- **Remote Management**: Configured and maintained via SSH login (manual monitoring, logs, token resets)
- **Domain**: Custom domain pointing to Mastodon instance, served over HTTPS
- **Bot Runtime**: Python bot script executed on the same server, using Mastodon API token auth

---

## 📜 Example Flow

1. User on Mastodon mentions bot with a format like:  
   `@Tweets_bot -uid some_user 2022-01-01 Y`
2. Bot scrapes tweets from `@some_user` since Jan 1st
3. Bot translates the tweet text if requested
4. Bot posts results as direct messages back to the user

---

## 🧠 Reflection

This project was my first experience with:

- 🧩 Full-stack bot interaction: from content parsing to remote API posting
- 🚀 Self-deploying and managing a Mastodon instance using **Docker**
- 🔐 Running remote services via **SSH + Linux VPS**
- 🧪 Handling real-world tweet data, emoji, timestamps, and translation
- 🧠 Designing a simple command language (`-uid`, `-word`) to interface with my bot

Though the tool is deprecated, I’m proud of what I built at the time and how it shaped my current understanding of automation, infrastructure, and modular architecture.

