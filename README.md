# Self-Disclosure & Job Search Assistant for People with Disabilities

I built this because navigating disability disclosure at work is genuinely confusing. There's a lot of legal language, conflicting advice, and no easy place to just ask a question and get a straight answer.

This app tries to fix that.

## What it does

It's a simple web app with three tools on one page, built specifically for job seekers on the Our Ability platform.

**Ask about self-disclosure** — Not sure when or how to tell your employer about your disability? Type your question, pick a category, and you'll get a short, honest answer backed by real sources from the web. No walls of text.

**Ask about accommodations** — Same thing, but for ADA workplace rights. What can you ask for? What's an employer required to do? Ask it like you'd ask a friend.

**Find jobs** — Describe yourself in plain English. The app figures out what job titles fit you and pulls matching listings from Our Ability's job board.

## How I built it

When you ask a question, the app does a live Brave web search using your question and category. The top results go straight to Claude, which reads them and writes a focused answer, under 80 words, with no jargon. Sources are always included so you can verify anything.

For job search, Claude reads your free-text description and pulls out 2-4 job keywords. Those hit the Our Ability job API and return real listings.

There's also video generation (Google Veo turns any answer into a short explainer clip) and an SMS system that sends job alerts and weekly check-ins via Twilio.

## Stack

- Python + FastAPI, deployed on Vercel
- Claude (Anthropic) for Q&A and keyword extraction
- Brave Search for live web results
- Our Ability / JobSync API for job listings
- Google Gemini Veo for video
- Twilio for SMS
- Plain HTML, CSS, and vanilla JS — no framework, no build step

## Try it live

https://self-disclosure-disability-qa.vercel.app

---

> Source code is proprietary (company project). This README covers how it works and the decisions behind it.
