# 🧠 Intelligence AI

> AI Research Thread Generator - Making cutting-edge ML papers accessible to practitioners

[![Twitter Follow](https://img.shields.io/twitter/follow/intelligence_ai?style=social)](https://twitter.com/intelligence_ai)
[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)]()

---

## 📖 About

**Intelligence AI** is an automated AI research content engine that discovers breakthrough papers, processes them with LLMs, and generates digestible Twitter threads for ML engineers and AI enthusiasts.

We bridge the gap between academic research and practical implementation by:
- 🔍 Discovering papers from arXiv, major AI labs, and research communities
- 🤖 Processing with Google Gemini to extract key insights
- 📱 Generating 7-9 tweet threads optimized for engagement
- ✅ Maintaining technical accuracy with honest limitations

**Target Audience:** ML engineers, AI researchers, tech enthusiasts (intermediate to advanced)

---

## 🎯 Key Features

### 🔬 Multi-Source Discovery
- **arXiv**: cs.AI, cs.LG, cs.CL, cs.CV categories (last 7 days)
- **Lab Blogs**: Anthropic, OpenAI, DeepMind, Meta AI, Google Research
- **Community**: Reddit (r/MachineLearning, r/LocalLLaMA)
- Smart deduplication via SQLite memory

### 🧵 Thread Generation
- **7-9 tweet format** with clear structure:
  - Hook (results-first, not method)
  - Problem/Context
  - Key findings (2-3 technical contributions)
  - Implications for practitioners
  - Paper link + attribution
  - ELI5 summary for accessibility
  - Engagement question
  - "Learn More" topics
- **Technical accuracy**: Exact numbers, benchmark conditions, limitations
- **Attribution**: Always credits original authors

### 📊 Content Quality
- Peer-reviewed or major lab papers only
- Avoids hype and unsubstantiated claims
- Distinguishes verified results from speculation
- Notes if code/models are available

### 🎛️ Automation
- Scheduled discovery (daily at 6am)
- Automated posting (8am, 12pm, 6pm)
- Queue management (4-day buffer)
- Cost-effective: ~$0.0006 per thread

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| **Content Discovery** | arXiv API, RSS feeds (feedparser), Reddit API (praw) |
| **AI Processing** | Google Gemini 2.0 Flash |
| **Thread Generation** | Custom prompt engineering with brand personality |
| **Storage** | SQLite (deduplication), CSV (queue) |
| **Posting** | Twitter API v2 |
| **Scheduling** | Cron jobs |
| **Language** | Python 3.8+ |

---

## 📋 How It Works

```
┌─────────────────┐
│  Paper Sources  │
│ (arXiv, Labs,   │
│  Reddit)        │
└────────┬────────┘
         │
         v
┌─────────────────┐
│ Discovery Engine│
│ (Filter & Rank) │
└────────┬────────┘
         │
         v
┌─────────────────┐
│  Gemini 2.0     │
│  (Extract Key   │
│   Insights)     │
└────────┬────────┘
         │
         v
┌─────────────────┐
│ Thread Builder  │
│ (7-9 Tweets)    │
└────────┬────────┘
         │
         v
┌─────────────────┐
│  Queue Manager  │
│ (Schedule Post) │
└────────┬────────┘
         │
         v
┌─────────────────┐
│  Twitter API    │
│ (Publish)       │
└─────────────────┘
```

---

## 📝 Example Thread

**Hook Tweet:**
> 🧵 DeepMind just cut protein folding compute by 40% while beating AlphaFold 2. Here's how:

**Context:**
> The challenge: Protein structure prediction is computationally expensive, limiting accessibility for smaller labs

**Key Finding:**
> They use a hierarchical attention mechanism that processes amino acid chains in chunks, reducing quadratic complexity

**Results:**
> 94.2% accuracy on CASP15 benchmark, 40% faster inference, runs on consumer GPUs

**Implications:**
> This could enable on-device protein analysis for drug discovery startups

**Attribution:**
> Paper: arxiv.org/abs/xxxx by Smith et al. at DeepMind

**ELI5:**
> Scientists found a faster way to predict how proteins fold (like origami but for molecules). This matters because knowing protein shapes helps create new medicines. The new method is 40% faster and works on regular computers.

**Engagement:**
> What would you build with cheaper protein folding? 👇

**Learn More:**
> Want to really understand this? Look up: protein folding problem, attention mechanisms in ML, AlphaFold, computational biology #MachineLearning #AI

---

## 🎨 Brand Voice

**Personality:** Knowledgeable AI researcher who makes complex papers accessible

**Characteristics:**
- Technically accurate but accessible
- Highlights practical implications
- Acknowledges limitations honestly
- Links to original sources
- Respects researcher attribution
- Leads with RESULTS, not methods

**Don't:**
- Hype or exaggerate
- Use jargon without explanation
- Bury the lede in technical details
- Skip attribution
- Make unsubstantiated predictions

---

## 📊 Performance Metrics

| Metric | Current | Target (90d) |
|--------|---------|--------------|
| **Threads/Week** | 21 | 21 |
| **Avg. Engagement Rate** | 2.5% | 4% |
| **Followers** | Growing | 5,000 |
| **Cost/Month** | $0.05 | $5 budget |

---

## 🚀 Setup & Usage

### Prerequisites
- Python 3.8+
- Google Gemini API key
- Twitter API credentials (optional for posting)

### Installation

```bash
# Clone repository
git clone https://github.com/yourusername/intelligence-ai

# Install dependencies
pip install -r requirements.txt

# Configure environment
cp .env.example .env
# Add your GEMINI_API_KEY
```

### Run Paper Discovery

```bash
# Dry run (see what would be processed)
python engines/paper_processor.py --brand intelligence_ai --dry-run

# Process papers and generate threads
python engines/paper_processor.py --brand intelligence_ai
```

### Post to Twitter

```bash
# Dry run
python engines/poster.py --brand intelligence_ai --platform twitter --dry-run

# Live posting
python engines/poster.py --brand intelligence_ai --platform twitter
```

### Schedule with Cron

```bash
# Paper discovery - daily at 6am
0 6 * * * /path/to/venv/bin/python engines/paper_processor.py --brand intelligence_ai

# Twitter posting - 8am, 12pm, 6pm
0 8,12,18 * * * /path/to/venv/bin/python engines/poster.py --brand intelligence_ai --platform twitter
```

---

## 📁 Project Structure

```
intelligence_ai/
├── config.json              # Brand configuration
├── personality.txt          # Thread generation prompt
├── sources.json             # arXiv categories, RSS feeds
├── queue.csv                # Scheduled posts
├── memory.db                # Processed papers (dedup)
├── posted_archive/          # Historical posts
└── README.md                # This file
```

---

## 💰 Cost Breakdown

### Gemini API (Thread Generation)
- **Model**: gemini-2.0-flash
- **Cost per thread**: ~$0.0006
- **Monthly (90 threads)**: ~$0.054

### Twitter API
- **Free tier**: 1,500 tweets/month
- **Usage**: ~270 tweets/month (90 threads × 3 tweets avg)
- **Cost**: $0

**Total Monthly Cost**: ~$0.05

---

## 🔧 Configuration

Edit `config.json` to customize:

```json
{
  "posting_schedule": {
    "times": ["08:00", "12:00", "18:00"]
  },
  "content_pillars": {
    "paper_threads": {
      "weight": 0.80,
      "focus": ["breakthrough_papers", "sota_results"]
    }
  },
  "processing": {
    "gemini_model": "gemini-2.0-flash",
    "max_papers_per_run": 12
  }
}
```

Edit `personality.txt` to change:
- Tone and style
- Thread structure
- What to emphasize
- Hashtag strategy

---

## 📈 Roadmap

- [x] Multi-source paper discovery
- [x] Gemini-powered thread generation
- [x] Automated posting to Twitter
- [x] Quality validation & filters
- [ ] LinkedIn support
- [ ] Instagram carousel generation
- [ ] Analytics dashboard
- [ ] A/B testing for hooks
- [ ] Community-sourced paper suggestions

---

## 🤝 Contributing

Contributions welcome! Areas of interest:
- New paper sources (academic databases, conferences)
- Improved prompt engineering for threads
- Analytics and performance tracking
- Platform integrations (LinkedIn, Medium)

---

## 📄 License

MIT License - See LICENSE file for details

---

## 🔗 Links

- **Twitter**: [@intelligence_ai](https://twitter.com/intelligence_ai)
- **Example Threads**: [See posted_archive/](posted_archive/)
- **Documentation**: [Full README](README.md)

---

## 💡 Inspiration

Built to solve a real problem: keeping up with AI research is overwhelming. We distill the signal from the noise and make breakthrough papers accessible to everyone.

**Quality over quantity. One well-crafted thread > five shallow summaries.**

---

Made with 🧠 by the Intelligence AI team
