---
layout: post
title: 🛠️ Building a card game with instant feedback using Firebase Realtime DB
date: 2023-10-27
---

# 🎉 Solo Cartas Malas

[**Solo Cartas Malas**](https://solocartasmalas.netlify.app/) uses Firebase Realtime DB to let multiple people play a game of Cards Against Humanity online.

## 🚀 Inception

I wanted to play a Spanish version of CAH to practice my Spanish with friends. I knew Firebase used nosql dbs and thought that storing all of the questions and answers in a json file and uploading it might be an easy approach. After I got the hang of CRUDing the player's hand with cards it became a breeze to add all of the relevant db listeners for changes in the db so that users could interact with each other instantly. Next, I had to create my cards. Putting existing cards into Google Translate wouldn't be good enough because these types of games rely on a language's nuance so a direct translation just isn't funny. To solve this I thought up a rule set to make sure prompts and responses matched up grammatically and then I was able to think up my own cards and also use ChatGPT to generate some ideas. Since ChatGPT "speaks" Spanish it was able to create some really funny cards I ended up putting in. It was great practice for my Spanish. Finally, After I had enough cards in a list I was able to prompt ChatGPT to speedily format my list into a json file which I uploaded to the NoSQL DB directly.

Warning! These are using Cards Against Humanity style cards, meaning most of the content is very, very inappropriate.

## 🧠 What I Learned

- **Firebase Realtime DB**
- NoSQL DB rules and concepts
- Next JS (SSG)
- React (continued practice)
