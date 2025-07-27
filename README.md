<div align="center">
    <h1> <img src="https://github.com/default-cybe/passwordless-auth/blob/main/assets/img/images/icon.png" width="80px"><br/>Passwordless Authentication</h1>
</div>
<p align="center"> <a href="https://github.com/default-cybe" target="_blank"><img alt="" src="https://img.shields.io/badge/Website-EA4C89?style=normal&logo=dribbble&logoColor=white" style="vertical-align:center" /></a> <a href="https://twitter.com/default_yt_" target="_blank"><img alt="" src="https://img.shields.io/badge/Twitter-1DA1F2?style=normal&logo=twitter&logoColor=white" style="vertical-align:center" /></a> <a href="https://www.instagram.com/kaivalya_ahir" target="_blank"><img alt="" src="https://img.shields.io/badge/Instagram-E4405F?style=normal&logo=instagram&logoColor=white" style="vertical-align:center" /></a> <a href="https://www.linkedin.com/in/kaivalya-ahir/" target="_blank"><img alt="" src="https://img.shields.io/badge/LinkedIn-0077B5?style=normal&logo=linkedin&logoColor=white" style="vertical-align:center" /></a> </p>

# Passwordless Authentication

Log in without ever typing a password. Instead of asking for one, the app looks
at a handful of signals about the login attempt (cookies, rough location, IP
address, a device fingerprint, and past browsing history) and rolls them into a
trust score. If the score is high enough you go straight in. If it isn't, you
get asked for a second factor first.

The reasoning is pretty simple: passwords get phished and reused all the time,
so it leans on "does this look like the same person on the same device" instead.

# Description

This is a demo of that flow. Every login attempt gets scored, and the score
decides whether the user is trusted right away or has to prove themselves with
an extra check.

# Features

* Log in with no password at all.
* A trust score built from cookies, location, IP, device fingerprint, and history.
* When the score comes back too low, it falls back to two-factor auth (or another check) before letting you in.

# Tech Used

![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![Bootstrap](https://img.shields.io/badge/bootstrap-%23563D7C.svg?style=for-the-badge&logo=bootstrap&logoColor=white)

# How it works

This is a static front-end (HTML/CSS/JS) backed by Firebase Authentication and
Realtime Database, so there is no server to run. `index.html` checks the Firebase
auth state and routes the user to `login.html` / `register.html` or, once
authenticated, to `home.html`. `advanced-auth.html` holds the adaptive
trust-score flow that decides when to ask for a second factor.

# Running locally

1. **Clone and enter the project:**
   ```bash
   git clone https://github.com/default-cybe/passwordless-auth.git
   cd passwordless-auth
   ```

2. **Add your Firebase config:**
   ```bash
   cp assets/js/firebase-config.example.js assets/js/firebase-config.js
   ```
   Fill in the values from Firebase console → Project settings → Your apps →
   SDK setup. This file is gitignored so your project's config stays out of the
   repo.

3. **Serve the files** (any static server works):
   ```bash
   python3 -m http.server 8000
   ```
   Then open `http://localhost:8000/index.html`.

# Security notes

- Firebase web API keys are **not secrets**. They ship in client code by
  design. Real access control comes from **Firebase Security Rules** and from
  **restricting the API key** in the Google Cloud console. Lock both down before
  exposing a project.
- The trust score is computed client-side for this demo. A production system
  would score server-side (a client can tamper with anything in the browser).

