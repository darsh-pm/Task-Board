# Darsh Task Board

A full-stack task management app built to practice React, 
Supabase, and AI integration.

## Live Demo
https://darshan2study-cpu.github.io/Task-Board/

## Features
- Three-column Kanban board (To Do / In Progress / Done)
- Card detail view with description, subtasks, priority and due date
- Drag and drop to move tasks between columns
- Overdue task filter
- AI prioritization via Groq (Llama 3.3) — analyzes open tasks 
  and recommends what to focus on first
- Email authentication with per-user data isolation (Supabase RLS)
- Persistent data across devices via Supabase

## Stack
- React (via CDN, no build step)
- Supabase (PostgreSQL database + Auth + Row Level Security)
- Groq API (Llama 3.3-70b)
- Tailwind CSS
- GitHub Pages

## Architecture
Frontend React app → Supabase database (per-user RLS) → Groq AI API

Authentication uses Supabase Auth with Row Level Security policies 
ensuring users only see their own tasks. AI feature sends active 
task data to Groq and returns prioritized recommendations.

## Planned Enhancements
- Activity log per card
- Supabase Edge Function to secure Groq API key
- Mobile drag and drop support
