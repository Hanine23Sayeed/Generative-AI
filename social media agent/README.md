# Social Media Content Generator
Turn YouTube videos into ready-to-post social media content in seconds! This project uses an autonomous AI agent powered by GPT-4o to read video transcripts,
generate platform-specific posts, and optionally enrich them with up-to-date web information. Perfect for marketers, content creators, and social media enthusiasts.

# Features
1- Autonomous AI Agent: The app uses a custom agent (content_writer_agent) that can decide how to generate posts based on video transcripts.
2- Multi-Platform Content: Generate posts tailored for LinkedIn, Instagram, and Twitter.
3- Smart Content Generation: GPT-4o creates engaging, readable, and platform-optimized posts.
4- Web-Enriched Posts: Optional web search for up-to-date details.
5- Downloadable Outputs: Export each generated post as a .txt file.
6- Asynchronous Processing: Fast, smooth, and responsive user experience.
7 -Custom Queries: Ask the agent for specific post styles or tones.

| Technology                 | Purpose                                     |
| -------------------------- | ------------------------------------------- |
| **Python 3.11+**           | Core programming language                   |
| **Streamlit**              | Interactive web app UI                      |
| **OpenAI GPT-4o**          | Powers the autonomous content-writing agent |
| **YouTube Transcript API** | Fetch video transcripts automatically       |
| **Asyncio**                | Handle asynchronous operations efficiently  |
| **Python-dotenv**          | Manage environment variables securely       |
