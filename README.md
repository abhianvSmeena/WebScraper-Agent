WebScraper Agent - Stealthy News Aggregator

Your personal news WebScraper Agent that silently gathers headlines and Reddit reactions, then generate audio.

---
FEATURES
- Scrape premium news websites (bypassing paywalls)
- Extract live Reddit reactions (even from JS-heavy threads)
- AI-powered audio summaries (text-to-speech with ElevenLabs)
- Real-time updates (thanks to Bright Data's MCP magic)

---
PREREQUISITES
- Python 3.9+
- Bright Data account (https://brightdata.com)
- ElevenLabs account (https://elevenlabs.io)

---
QUICK START

1. Clone the repo
```
https://github.com/abhianvSmeena/WebScraper-Agent.git
cd WebScraper-Agent
```

2. Install Dependencies
```
pip install -r requirements.txt
```

3. Ninja Secrets (Environment Setup)
Create virtual env file:
```
python -m venv venv
```

Configure your secrets in .env:
```
# Bright Data
BRIGHTDATA_MCP_KEY="your_mcp_api_key"
BROWSER_AUTH="your_browser_auth_token"

# ElevenLabs 
ELEVENLABS_API_KEY="your_text_to_speech_key"
```

4. Prepare Your Weapons (Bright Data Setup)
- Create MCP zone: https://brightdata.com/cp/zones
- Enable browser authentication
- Copy credentials to .env

---
RUNNING THE WebScraper-Agent

First terminal (Backend):
```
python run backend.py
```

Second terminal (Frontend):
```
streamlit run frontend.py
```

---
PROJECT STRUCTURE
```
.
├── frontend.py          # Streamlit UI
├── backend.py           # API & data processing  
├── utils.py             # UTILS  
├── news_scraper.py      # News Scraper  
├── reddit_scraper.py    # Reddit Scraper  
├── models.py            # Pydantic model
├── .env                 # Secret map template
└── requirements.txt     # Alternative dependency list
```

---
NOTES
- First scrape takes 15-20 seconds
- Reddit scraping uses real browser emulation via MCP
- Keep .env file secret

---
SUPPORT
Open an issue: https://github.com/yourusername/NewsNinja/issues
Bright Data support: https://brightdata.com/support

*"In the darkness of information overload, be the ninja."* 🌑
