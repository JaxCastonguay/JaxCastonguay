---
layout: post
title: 🛠️ Building a card game with instant feedback using Firebase Realtime DB
date: 2023-10-27
---

# 🎉 Only Bad Cards

[**Only Bad Cards**](https://onlybadcards.netlify.app/) uses Firebase Realtime DB to let multiple people play a game of Cards Against Humanity Online.

## 🚀 Inception

I wanted to play a Spanish version of CAH to practice my Spanish with friends. I knew Firebase used nosql dbs and thought that storing all of the questions and answers in a json file and uploading it might be an easy approach. After I got the hang of CRUDing the player's hand with cards it became a breeze to add all of the relevant db listeners for changes in the db so that users could interact with each other instantly. In the end, I have yet to translate a sufficient amount of cards to play the game in Spanish because the "nuance" of CAH's cards are often lost in translation, but I was really proud of the work I had done creating the web app so I wanted it to be available to anyone who finds it.

Wow they just let you use all their cards? Yes, see [here](https://www.cardsagainsthumanity.com/terms-of-use) (under "License")

Warning! These are using real Cards Against Humanity cards, meaning most of the content is very inappropriate.

## 🧠 What I Learned

- **Firebase Realtime DB**
- Next JS (SSG)
- React (continued practice)
