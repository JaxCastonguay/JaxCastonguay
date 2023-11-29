---
layout: post
title: 🛠️ Use AI to Generate Custom User Specific Podcasts
date: 2023-11-28
---

# 🎉 Pod Persona

[**Pod Persona**](https://podpersona.netlify.app/) uses Open AI's API and Firebase serverless architecture to create Podcasts tailored to YOUR interests

## 🚀 Inception

I'll admit it, I'm a headline only reader. But I'm trying to get better. The idea was simple in my head:

- Grab an article.
- Scrape the text.
- Summarize with AI.
- Translate to Spanish with AI - nary a project I do doesn't shoe horn language learning in somehow.
- Use Open AI's wonderful new text to speech API to get a natural, not robot-y, sounding mp3 file.
- Store audio files and data throughout the day and splice them together at the end.
- Give user a self-tailored podcast of all their articles they added throughout the day.
  But in practice I ran into quite a few headaches.
- Had to store tokenizers for a natural language processor grabbing the articles (NTLK/punkt) in order to not have to download punkt on every server call (expensive compute time)
- Pydub, which I used for splicing audio files together, relied on ffmpeg and ffprobe. This caused zero issues on my Windows machine, but I had to store and point to the binary files when running my functions on firebase (Linux)
- Audio bugs when splicing files together that had slightly different metadata

In the end, I really liked my design. I let authenticated users add articles and podcast generations requests to the DB via button click and then use Firebase Function's on_create feature to detect requests and complete the work in the background. This meant users could dump links throughout the day and not have to wait on a pesky loading screen before adding another article or exiting out of the app. By the time a user wanted to generate their podcast, they would get in only a few seconds because the audio was already created and only needed to be stitched together.

## 🧠 What I Learned (New)

- Firebase Serverless Functions
- Firebase Firestore
- Firebase Storage
- Firebase Auth

## 🧠 What I Learned (Continued Practice)

- Open AI API
- NoSQL DB rules and concepts
- Next JS (SSG)
- React
- Python
- Typescript
