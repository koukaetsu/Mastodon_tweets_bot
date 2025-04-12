# 🐦 Tweets-to-Mastodon Bot (2022 Archive)

> ⚠️ This script is no longer in use. It was originally built in 2022 as an early project during my self-learning of Python automation, web scraping, and bot communication via API.  
> I'm keeping it here as a personal record of my development progress.

---

## 💡 Project Summary

This Python bot monitors specific Twitter users' activity, optionally translates the content, and automatically reposts it to a Mastodon account via direct messages.

🛠️ It was deployed and operated on **a self-hosted Mastodon instance** running on **my own VPS and custom domain**, which I configured and maintained independently.

The bot simulated cross-platform "tweet forwarding" before Twitter API limitations and server costs led to the instance being shut down.

---

## 🛠️ Features

- ✅ Uses [`Scweet`](https://github.com/Altimis/Scweet) to scrape tweets by user and time range
- 🌐 Optional content translation using `google_trans_new`
- 📤 Posts results as **direct messages (DM)** to users on Mastodon
- 📥 Recognizes commands via content pattern matching in `on_update`
- 🔁 Supports translation mode (`Y/N`) and multiple forwarding options

---

## 🖥️ Deployment Details

- Platform: **Mastodon (custom instance)**
- Hosting: **VPS (cloud server) configured manually**
- Domain: **Self-owned domain pointing to instance**
- Security: Used token-based Mastodon API authentication
- Maintenance: Regularly updated + monitored by me during runtime

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

- Full-stack bot interaction: from input parsing to API execution
- Building and maintaining my own Mastodon instance (server + domain + database)
- Handling real-world content (tweet scraping, unicode, timestamps)
- Writing my own command parsing structure using regex

Though the tool is deprecated, I’m proud of what I built at the time and how it shaped my current approach to modular design, deployment, and automation.
