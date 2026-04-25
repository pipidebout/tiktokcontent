# TikTok Developer App Approval - Video Script

Screen-capture walkthrough 

---

## 1. Use Case

Personal pipeline for automating TikTok uploads of rendered Gregorian chant shorts from my own channel.

---

## 2. OAuth Flow (Login Kit + user.info.basic)

```bash
yarn tiktok:auth
```

Creator authorizes once via TikTok's own OAuth page; token is stored locally and refreshed automatically.

---

## 3. Upload Flow (Content Posting API + video.publish)

```bash
yarn pipeline:tiktok --channel monastic-echo --item-id me-20260419-073
```

App uploads a rendered MP4 to the creator's own account - no other accounts, no posting on behalf of others.

---

## 4. Token / Permission Model

Only `user.info.basic` and `video.publish` scopes are requested. No follower data, no DMs, no other users' content.

---

## 5. Scope of Use

This is a single-creator tool - no end-users, no SaaS, just the creator publishing to their own channel.

