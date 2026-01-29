# 🧠 Intelligence AI

> A personal bot I built to stay current with AI research without drowning in papers, threads, and hype.

People might call it an agent, but I’m not fully convinced where true autonomy begins and supervised workflows end. For now, this is very much a bot — opinionated, constrained, and intentionally supervised.

I’d rather go rogue with a bot than let an agent go rogue on my behalf 😉

[![Twitter Follow](https://img.shields.io/twitter/follow/_IntelligenceAI?style=social)](https://x.com/_IntelligenceAI)
[![Status](https://img.shields.io/badge/status-live-success.svg)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)]()

---

## 📌 TL;DR

I built a bot that:
- Scans AI research sources daily (arXiv, lab blogs, communities)
- Picks breakthrough papers worth reading
- Breaks them down into digestible Twitter threads
- Posts 3x daily so I don't miss what matters

**Why?** Reading 50+ papers/week isn't realistic. This filters signal from noise.

**Live:** [@_IntelligenceAI](https://x.com/_IntelligenceAI)

---

## 🎯 The Personal Problem it is solving:

I wanted to stay current with AI research, but:
- arXiv publishes 100+ ML papers daily
- Most aren't relevant to practitioners
- Academic abstracts bury the actual impact
- No time to filter what's worth deep-diving

**Solution:** A bot that curates, summarizes, and points me to papers,new releases in AI,and the latest relevant news I should actually read.

---

## 💡 What It Does

**For Me:**
1. Discovers papers from trusted sources (arXiv categories, DeepMind, OpenAI, Anthropic, etc.)
2. Filters out noise (preprints without validation, hype without substance)
3. Extracts what matters: results, implications, limitations
4. Formats as Twitter threads: scannable, technical but accessible
5. Includes "Learn More" pointers if I want to deep-dive

**Format:**
- 7-9 tweet threads, but uses intelligence to decide on relevance
- Qualification is Results-first (not method-first - Impact matters)
- Always includes limitations (builds trust)
- Links to original paper
- ELI5 for broader understanding

**Why Twitter?** That's where I already consume tech content. Native format = easier to scan during commute/breaks.

---

## 📊 Performance & Reach

### Target Metrics
| Metric | Value | Why It Matters |
|--------|-------|----------------|
| **Threads/Week** | 21 | Consistent cadence |
| **Engagement Rate** | 2.5% → 4% target | Quality filtering drives this |
| **Follower Growth** | Organic | Zero paid acquisition |
| **Reach** | ~5K impressions/thread | Niche but relevant audience |
| **Cost** | $0.05/month | Runs on chai money |

### About Organic Growth

**Important context:** Building a large social following requires consistent human engagement - replies, conversations, networking. This bot focuses on **content quality over growth hacks**.

Large followings (50K+) need:
- Daily community engagement (replies, DMs)
- Relationship building with influencers
- Trending topic participation
- Time investment I'm not making

**My goal:** Serve practitioners(or wannabee's) who want curated research, not chase vanity metrics. Trust > scale. 

---

## 🛠️ How It Works (Abstract)

**Simple version:**
1. Bot scans research sources daily
2. Quality filters remove noise
3. AI extracts key insights
4. Formats as Twitter thread
5. Posts at optimal times (8am, 12pm, 6pm EST)

**That's it.** No fancy architecture needed - just consistent execution.

**Key decision:** Results-first formatting. Tested over 90+ threads - it outperforms method-first by 3x. Engineers care about *impact*, not *how*.

---

## 🧰 Tech Stack

**Tools I used to build this:**
- **Development:** Cursor (AI-assisted coding)
- **Content Generation:** Claude Sonnet 4.5, Google Gemini 2.0 Flash
- **Data Storage:** SQLite (deduplication)
- **Scheduling:** Python + cron jobs
- **Publishing:** Content Publish API v2
- **Language:** Python 3.8+

**Why these choices:**
- Cursor = faster development iteration
- Claude/Gemini = high-quality text processing at low cost
- SQLite = zero-config, perfect for side projects
- Python = quick prototyping, good API libraries

---

## 💰 Cost Efficiency

One of the surprising wins: **scalability at near-zero cost**.

- **Cost per thread:** ~$0.0006 (AI API usage)
- **Monthly cost:** ~$0.05 for 90 threads
- **Cost per follower:** Effectively $0 (organic)

**Why it matters:** I can 10x output without meaningful cost increase. This isn't a VC-funded operation - it's a side project that runs indefinitely on pocket change.

---

## 📈 What I Learned Building This

### 1. Distribution > Content Quality
Initial assumption: Great threads naturally spread.

Reality: Timing, consistency, and format matter more than perfection.

Learning: Reliable content at the right time > occasional brilliance.

### 2. User Feedback Without Surveys
I tracked *saves* and *bookmarks* (signal of value) instead of likes (vanity metric).

Results-first hooks got 3x more saves. ELI5 sections increased shares by 40%.

### 3. Trust = Acknowledging Limits
Adding "Limitations" sections to threads *increased* engagement. ML engineers distrust hype but respect honesty.

Product insight: Transparency builds trust in technical communities.

### 4. Automation ≠ Hands-Off
I still manually review 100% of threads before posting. The bot handles discovery and drafting; I handle nuance and quality control.

Lesson: AI augments judgment, doesn't replace it.

---

## 🎯 Content Strategy

### What Gets Posted
- Peer-reviewed papers or major lab publications only
- Results that matter to practitioners (not just academia)
- Honest limitations (builds credibility)
- Pointers to deeper reading

### What Gets Filtered Out
- Preprints without validation
- Hype-driven claims
- Unreproducible results
- Generic "AI is cool" content

### Why It Works
**Position:** Knowledgeable peer, not hype machine.

**Format:** Scannable threads that respect time. If you want depth, the paper link is there.

**Trust:** Never exaggerate. If a result is incremental, I say so.

---

## 🔗 Links

- **Live Bot**: [@_IntelligenceAI on X/Twitter](https://x.com/_IntelligenceAI)

---

## 💡 Why I Built This

**The Problem:** ML engineers want to stay current, but face information overload. Existing solutions are either too shallow (summaries miss nuance) or too time-consuming (reading papers isn't realistic).

**My Hypothesis:** An automated system could filter and distill papers if it prioritized *relevance* over *completeness*.

**What I Validated:**
- Engineers will engage with research threads if they're results-first and honest about limitations
- Consistent posting beats viral spikes for building trust
- Near-zero cost proves this scales

**What I Learned:**
- Content format is a product feature (structure = engagement)
- Reliability builds audience trust more than novelty
- Organic growth in technical communities requires patience

**Why Share This?**
I built it to solve my own problem, but the approach applies broadly: **product thinking applies to content**. Format, timing, and honesty are strategic decisions, not creative ones.

---

*A personal research tool by [Chirag Kankrecha](https://github.com/chirag-kankrecha) - Testing product strategy in content curation*
