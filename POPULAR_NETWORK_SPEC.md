# Popular Network — Full Project Specification

## For: Homer (OpenClaw AI Agent)
## Owner: Trevor
## Date: March 22, 2026
## Status: Pre-MVP / Pilot Planning

---

## TABLE OF CONTENTS

1. [Project Overview](#1-project-overview)
2. [Core Philosophy](#2-core-philosophy)
3. [What This Is NOT](#3-what-this-is-not)
4. [Key Stakeholders](#4-key-stakeholders)
5. [User Experience Vision](#5-user-experience-vision)
6. [Primary User Intent Categories](#6-primary-user-intent-categories)
7. [Feature Ecosystem (Full Scope)](#7-feature-ecosystem-full-scope)
8. [Homepage Architecture](#8-homepage-architecture)
9. [Dynamic Landing Pages](#9-dynamic-landing-pages)
10. [Technical Architecture](#10-technical-architecture)
11. [Data Architecture](#11-data-architecture)
12. [Data Ingestion Strategy](#12-data-ingestion-strategy)
13. [API Integrations](#13-api-integrations)
14. [Business Onboarding Flow](#14-business-onboarding-flow)
15. [Publisher Workflow](#15-publisher-workflow)
16. [AI Content Generation](#16-ai-content-generation)
17. [Revenue Model](#17-revenue-model)
18. [Network Vision (Scaling)](#18-network-vision-scaling)
19. [News Strategy](#19-news-strategy)
20. [Youth Sports Module](#20-youth-sports-module)
21. [Camera & Streaming Systems](#21-camera--streaming-systems)
22. [Rewards & Loyalty System](#22-rewards--loyalty-system)
23. [Travel Mode](#23-travel-mode)
24. [Community Chat](#24-community-chat)
25. [Naming & Domain Strategy](#25-naming--domain-strategy)
26. [Risks & Mitigations](#26-risks--mitigations)
27. [Known Gaps & Open Questions](#27-known-gaps--open-questions)
28. [Phased Build Plan](#28-phased-build-plan)
29. [MVP Definition (Phase 1)](#29-mvp-definition-phase-1)
30. [Database Schema (Starting Point)](#30-database-schema-starting-point)
31. [File & Folder Structure (Suggested)](#31-file--folder-structure-suggested)

---

## 1. PROJECT OVERVIEW

The Popular Network is an AI-first community platform that replaces the fragmented local internet (news sites, Facebook groups, Craigslist, Yelp, event calendars, weather apps) with a single, chat-driven "local operating system."

Users ask natural language questions and receive structured answers powered by local data — news, businesses, events, weather, classifieds, jobs, real estate, and more.

The platform is designed to be licensed territory-by-territory to newspaper publishers who become local operators. The company builds and controls the platform layer and national ad network above them.

### One-Sentence Summary

> Replace browsing local news sites with asking your local community AI everything — and getting answers powered by your newspaper.

### Core Identity

This is a **community operating system** combining:
- Information (news, weather, alerts)
- Commerce (businesses, classifieds, jobs, real estate)
- Engagement (events, chat, polls, games, rewards)
- AI automation (content generation, data aggregation, smart responses)

---

## 2. CORE PHILOSOPHY

- **AI-first**: The chatbot IS the product, not a feature bolted onto a website
- **Local-first**: Each deployment serves a specific geographic territory
- **Networked**: Individual deployments connect into a regional and national network
- **Revenue-integrated**: Monetization is baked into the UX, not an afterthought
- **Publisher-powered**: Local newspapers operate and sell the platform in their markets
- **Local control + Network efficiency**: Publishers own their territory; the platform provides the tools

### Design Philosophy: Newspaper + AI Hybrid

| Old Model | New Model |
|-----------|-----------|
| Browse | Ask |
| Click links | Get answers |
| Static layout | Dynamic feed |
| Ads sidebar | Intent-driven recommendations |
| Support chatbot | AI IS the homepage |

---

## 3. WHAT THIS IS NOT

- NOT a better newspaper website
- NOT a CMS
- NOT a chatbot widget added to an existing site
- NOT Quadd.ai (Trevor's separate existing project — completely unrelated)
- NOT an incremental improvement to existing local news sites

This IS:
- A new platform / ecosystem
- A local AI operating system for daily life
- The AI-powered digital infrastructure for local communities

---

## 4. KEY STAKEHOLDERS

### Founding Team
- **Trevor** — Product vision, strategy, publisher (Windom)
- **Nate** — Technical lead, built initial prototype
- **John Draper** — Publisher (Pipestone County Star)

### Founding Team Gaps Identified
- Product owner / UX lead
- Operations / onboarding
- Sales / revenue scaling
- Marketing / growth
- Business development / data partnerships
- Legal / compliance (advisor level)

### Pilot Group: Southwest Peach
- A shared publication inserted across multiple newspapers
- Covers: Westbrook, Marshall, Pipestone, and surrounding smaller communities
- Already a connected network with existing content-sharing model
- Selected as Phase 1 pilot environment

---

## 5. USER EXPERIENCE VISION

### Chat-First Interface

Users interact primarily through a conversational AI interface. Examples:
- "Are there any flower specials?"
- "What's happening tonight?"
- "Any jobs within 30 miles?"
- "Find me a plumber"
- "Homes under $300k"
- "What should I do this weekend?"

### AI Response Format (Hybrid Output)

Every query returns a combination of:

1. **Chat summary** — Natural language answer from the LLM
2. **Structured UI cards** — Events, businesses, listings, news articles displayed as visual cards
3. **Maps** — When location-relevant
4. **Quick actions** — Call, Visit Website, Save, Get Directions
5. **Links to full landing pages** — Dynamically generated detail pages

### UX Principles
- Simple entry (chat box is the primary interaction)
- AI-driven backend handles routing, search, and presentation
- One-stop platform (replaces multiple apps/sites)
- Personalized experience based on user behavior and preferences
- The interface should feel like ChatGPT / Perplexity / Google Discover blended with a local newspaper

---

## 6. PRIMARY USER INTENT CATEGORIES

These are the top-level reasons users visit the platform. Each represents a daily habit trigger. **Do NOT mix subcategories with primary categories** — keep the hierarchy clean and scalable.

### Category 1: News
**Motivation:** Stay informed about the local area
- Breaking / Latest News
- Local Sports
- Human Interest Stories
- Opinion / Editorials
- Obituaries
- Police reports
- Legals

### Category 2: Advertising / Commerce
**Motivation:** Buy, sell, or discover products/services
- Automobiles
- Boats / Recreational Vehicles / ATVs
- Real Estate
- Home & Garden
- Jobs / Employment
- Local Services
- Retail / Deals
- Equipment
- Classifieds and garage sales

### Category 3: Community Events
**Motivation:** Know what is happening locally
- Event calendars
- Local activities
- Youth sports schedules
- Community gatherings

### Category 4: Weather
**Motivation:** Make daily decisions
- Hyper-local weather (per community)
- Radar maps
- Severe weather alerts
- Seasonal insights
- Road conditions

### Category 5: Community Chat
**Motivation:** Connect socially
- Local discussion
- Real-time conversation hub
- Community interaction
- Social layer of the platform

---

## 7. FEATURE ECOSYSTEM (FULL SCOPE)

This is the complete feature vision. NOT all of this ships in MVP. See Phase plan below for sequencing.

### Information Layer
- Local news (AI-generated + traditional)
- National/world news
- Weather
- Road conditions
- Alerts & notifications

### Commerce Layer
- Business directory (with reviews)
- Deals and specials
- Classifieds and garage sales
- Job listings (radius-based search)
- Real estate listings
- Vehicle listings
- CRM / inventory syncing for businesses

### Community Layer
- Events calendar
- Polls and engagement tools
- User-generated content
- Youth sports updates
- Community chat

### AI Content Layer
- Press releases → AI-generated stories
- Meeting minutes → AI-generated articles
- Audio → transcription + story generation
- Sports stats → AI-generated recaps

### Engagement Layer
- Games (crosswords, trivia)
- Contests and leaderboards
- Rewards and loyalty programs

### Media Layer
- Podcasts
- Video content
- AI summaries of long-form content

### Travel Mode (Future)
- Location-aware mobile experience
- Real-time recommendations while driving
- Audio responses

---

## 8. HOMEPAGE ARCHITECTURE

The homepage is structured in distinct layers:

### TOP — Trust & Familiarity Layer
- Publisher logo (e.g., Pipestone County Star)
- Date, weather widget
- Navigation (News, Sports, Obits, etc.)
- Featured story with hero image
- **Purpose:** Maintain credibility and brand equity from the newspaper

### MIDDLE — AI Discovery Layer (PRIMARY INTERACTION ZONE)
- Large conversational prompt input
- Suggested queries / prompt starters
- AI-generated results displayed as cards, maps, quick actions
- Dynamic, personalized, replaces traditional navigation
- **This is the core of the product**

### RIGHT SIDE — Monetization Layer
- Featured businesses (paid placements)
- Real estate listings
- Sponsored placements
- Job listings
- **Key: Everything here is queryable by the AI**

### LEFT / BELOW — Content Layer
- Traditional news feed
- Sports, Opinion, Obituaries
- **Secondary to AI discovery — still present for familiarity**

### BOTTOM / MODAL — Full Chat Interface
Two options explored:
- **Option A:** Expanding bottom panel (like Apple Maps / Spotify drawer)
- **Option B:** Full conversational modal takeover

Chat capabilities:
- Multi-turn conversation
- Context-aware results
- Mixed content responses (events, listings, articles, businesses)

---

## 9. DYNAMIC LANDING PAGES

Each user query can generate a dynamic landing page that includes:
- Relevant businesses matching the query
- Current specials and promotions
- Ads (contextual)
- AI-generated summary of results

### Premium vs Standard Listings
- **Paid businesses:** Enhanced placement, richer cards, featured position
- **Non-paying businesses:** Standard visibility, basic listing

---

## 10. TECHNICAL ARCHITECTURE

### Existing Prototype (Built by Nate)
- Basic AI text-prompt tool
- Early-stage data loaded: news content, business info, restaurant data
- Serves as proof of concept

### Existing Technical Capabilities
- RAG (vector search via ChromaDB)
- Modular data: articles, ads, events
- Chat engine
- Admin dashboard
- Ingestion pipelines

### Recommended Stack
- **Database:** PostgreSQL (structured data)
- **Vector Store:** ChromaDB (for RAG / semantic search)
- **LLM:** OpenAI or Claude API (for chat responses, content generation)
- **Backend:** Python or Node.js (TBD based on Nate's prototype)
- **Frontend:** Web-based (responsive for mobile), eventually native mobile app
- **CMS Strategy:** Headless CMS, API feed, or scraping fallback
- **Hosting:** Cloud (AWS, GCP, or similar)

### Multi-Tenancy Requirement
The platform MUST support multiple publishers, each with their own:
- Geographic territory
- Content library
- Business directory
- Branding (logo, colors)
- User base
- Revenue tracking

This is not a single-site deployment — it is a multi-tenant platform from the start.

---

## 11. DATA ARCHITECTURE

### Core Database Tables (PostgreSQL)

```
businesses
  - id, name, address, city, state, zip, phone, website, email
  - category, subcategory
  - description, hours, social_links
  - latitude, longitude
  - publisher_id (territory owner)
  - subscription_tier (free, basic, premium)
  - created_at, updated_at

events
  - id, title, description, location
  - start_date, end_date, start_time, end_time
  - category, cost, organizer
  - publisher_id
  - created_at, updated_at

news_articles
  - id, title, body, summary, author
  - category (news, sports, opinion, obituary, legal, police)
  - source (human, ai_generated, press_release)
  - publish_date
  - publisher_id
  - created_at, updated_at

classifieds
  - id, title, description, price, category
  - contact_info, location
  - user_id, publisher_id
  - expires_at
  - created_at, updated_at

job_listings
  - id, title, company, description
  - location, radius_miles, salary_range
  - category, contact_info
  - publisher_id
  - created_at, updated_at

real_estate_listings
  - id, address, price, bedrooms, bathrooms, sqft
  - description, photos, agent_info
  - listing_type (sale, rent)
  - publisher_id
  - created_at, updated_at

vehicle_listings
  - id, year, make, model, price
  - mileage, description, photos
  - dealer_or_private, contact_info
  - publisher_id
  - created_at, updated_at

social_posts
  - id, business_id, platform (facebook, instagram, x)
  - content, post_url, posted_at
  - created_at

locations
  - id, name, type (school, church, government, park)
  - address, latitude, longitude
  - publisher_id
  - description, website, phone

publishers
  - id, name, territory_name, territory_type (county, city, region)
  - logo_url, brand_colors
  - subscription_tier
  - created_at, updated_at

users
  - id, email, name, location
  - publisher_id (home territory)
  - subscription_tier (free, premium)
  - preferences (JSON)
  - created_at, updated_at

ads
  - id, business_id, publisher_id
  - ad_type (display, sponsored_response, featured_listing)
  - content, target_url, impressions, clicks
  - start_date, end_date
  - created_at, updated_at

weather_cache
  - id, location, data (JSON), fetched_at

chat_sessions
  - id, user_id, publisher_id
  - messages (JSON array)
  - created_at, updated_at
```

---

## 12. DATA INGESTION STRATEGY

### Business Backfill (Initial Population)
- **Google Places API** → Pull base business listings for a territory
- Auto-populate: name, address, phone, hours, categories, reviews, photos
- This gives the platform data on Day 1 before businesses sign up

### Website Scraping
- **Firecrawl** or custom scraper
- Pull business websites for menus, services, pricing, descriptions
- Keep listings fresh with periodic re-scraping

### Social Media Ingestion
- **Facebook Graph API** — posts, events, business pages
- **Instagram API** — posts, stories (if available)
- **Twitter/X API** — posts, mentions
- Store in `social_posts` table linked to `business_id`

### News Content Ingestion
- **API feed** (ideal — from publisher CMS)
- **RSS** (common fallback)
- **Scraping** (last resort)
- Newspaper PDFs can be processed with OCR + AI extraction

### Evergreen Local Data (Manual + Scraped)
- Schools, government offices, churches, parks
- Loaded into `locations` table
- Updated infrequently

### Content Input Requirements from Publishers
- Newspaper content (PDF or text/API)
- Business directories
- Community event data
- Restaurant listings
- Evergreen data (schools, government, churches)
- Ongoing content updates (frequency TBD per publisher)

---

## 13. API INTEGRATIONS

| API | Purpose |
|-----|---------|
| Google Places API | Business backfill, reviews, photos |
| OpenWeather API | Weather data per location |
| Facebook Graph API | Business social content, events |
| Instagram API | Business social content |
| Twitter/X API | Business social content |
| OpenAI / Claude API | LLM for chat, content generation, summaries |
| Stripe | Payment processing for subscriptions |
| SendGrid / Mailchimp | Email notifications, onboarding emails |
| Calendly | Scheduling (optional) |
| Firecrawl | Website scraping |
| ChromaDB | Vector embeddings for RAG search |

---

## 14. BUSINESS ONBOARDING FLOW

### Publisher-Side (Sales Flow)
1. Publisher enters business name into admin dashboard
2. System auto-fills business data via Google Places API + web scraping
3. System generates a draft listing
4. Publisher sends onboarding link to business owner

### Business-Side (Self-Service)
1. Business owner clicks onboarding link
2. Reviews and claims their listing
3. Connects social accounts via OAuth (Facebook, Instagram, etc.)
4. System stores OAuth tokens
5. Auto-sync begins — social posts, reviews, hours updates pulled automatically

### Goal: Minimal Manual Work
- One-field entry by publisher
- Auto data fill from APIs
- Automated onboarding emails
- AI-assisted listing optimization

---

## 15. PUBLISHER WORKFLOW

Publishers are the local operators. Their daily workflow includes:

### Content Management
- Upload/approve news articles
- Review AI-generated content before publishing
- Manage event calendar
- Moderate community submissions

### Sales & Revenue
- Sell business subscriptions (~$200/month estimated)
- Manage ad placements (featured listings, sponsored responses)
- Track revenue and performance

### Admin Dashboard Needs
- Content queue (articles pending review)
- Business directory management
- Ad management
- Analytics (traffic, engagement, revenue)
- User management

---

## 16. AI CONTENT GENERATION

The platform uses AI to transform raw inputs into publishable content:

### Input → Output Workflows
| Input | Output |
|-------|--------|
| Press release (text) | News article |
| Meeting minutes (text/PDF) | Summary article |
| Audio recording | Transcription + article |
| Sports box score / stats | Game recap article |
| Parent/coach upload (sports) | Youth sports recap |
| Business data | Business profile content |

### Human-in-the-Loop
- AI generates draft content
- Publisher reviews before publishing
- Flagged for editorial approval
- This addresses the "news desert" problem — communities without reporters can still get local coverage

---

## 17. REVENUE MODEL

### Three-Layer Revenue System

#### Layer 1: Local Ownership (Publisher Revenue)
- **Territory licensing fees** — Publishers pay for exclusive rights to a geographic territory (county-level)
  - One-time buy-in fee OR annual renewal
  - Tiered pricing based on market size
- **Business subscriptions** — ~$200/month per business
  - Includes: listing, social aggregation, chatbot integration, analytics
- **Premium business placements** — Featured listings, top-of-page exposure
- **Sponsored / native content** — Businesses pay for editorial-style stories
- **Lead generation** — AI routes users to businesses, collect leads via chatbot/forms
- **Events & promotions** — Shop Local campaigns, sponsored events, contests

#### Layer 2: Platform Services (SaaS Revenue)
- **Add-on services** — Hosting, data storage, AI processing tools, content distribution
- **Premium analytics packages** — Reader behavior, ad performance, engagement metrics
- **Training & onboarding** — Setup packages, AI adoption training, consulting
- **CRM / advertiser management** — Tools for publishers to manage their business clients

#### Layer 3: Network Monetization (National Revenue)
- **National advertising** — Sponsored responses, featured placements across all markets
  - Similar to Google Ads but embedded in localized AI-driven experiences
  - One ad slot per publisher reserved for national advertisers
- **Data aggregation** — Cross-market insights (anonymized)
- **Cross-market content distribution** — Shared job listings, shared ads

### Consumer Revenue
- **Premium subscription** — Full article access (vs AI summaries), podcasts, video, premium features
- **Ad-free experience** — Pay to remove ads
- **Exclusive content** — Early access, behind-the-scenes, premium editorial
- **Local sports streaming** — AI camera game streaming (future)
- **Personalized alerts** — Follow businesses, categories, topics

### Free Features (No Charge to Users)
- Basic classifieds
- Community posts
- Event browsing
- Weather
- Basic business search

---

## 18. NETWORK VISION (SCALING)

### Geographic Scale Path
```
Hyperlocal (single community)
  → Local (county)
    → Regional (multi-county cluster)
      → National (all territories)
```

### Network Effects
- Shared job listings across territories
- Shared classified listings (radius-based)
- National ad inventory sold across all markets
- Shared content distribution (regional/national stories)
- Cross-market analytics and insights

### Territory Strategy
- County-level exclusivity (one publisher per county)
- Creates scarcity and competitive value
- Builds a defensible network footprint
- Establishes ownership mentality among publishers

---

## 19. NEWS STRATEGY

### Addressing News Deserts
- Many communities have lost local newspapers
- Platform enables local coverage without full-time reporters
- Government, schools, and organizations submit content directly
- AI transforms submissions into publishable articles
- Human review required before publishing

### Content Sources
- Publisher-written articles (traditional journalism)
- AI-generated from press releases, meeting minutes, audio
- Community submissions (moderated)
- Aggregated from partner publishers in the network

---

## 20. YOUTH SPORTS MODULE

### Current Vision
- Parents and coaches upload game data (scores, stats, photos)
- AI generates game recaps automatically
- Published under the sports section

### Future Vision
- Live scoring integration
- AI-powered video tracking (via camera systems)
- Automated highlight generation
- Streaming for local games

---

## 21. CAMERA & STREAMING SYSTEMS

### Use Cases
- Youth and high school sports streaming
- City council / government meeting recording
- Community event streaming

### Hardware Tiers
| Tier | Cost Range | Use Case |
|------|-----------|----------|
| Entry-level | ~$250 | Basic recording, fixed camera |
| Mid-range | ~$1,000–$3,000 | Auto-tracking, better quality |
| Professional | ~$5,000–$7,000+ | Multi-camera, AI tracking, broadcast quality |

### AI Processing
- NVIDIA Jetson devices for edge AI processing (optional)
- Cloud AI for transcription, highlights, recap generation
- Integration with the platform's content pipeline

---

## 22. REWARDS & LOYALTY SYSTEM

### Concept
- Centralized rewards program across all local businesses
- Replaces multiple individual loyalty cards with one system
- QR-based redemption at participating businesses

### Value
- Drives repeat visits for businesses
- Increases platform engagement for users
- Levels playing field for small businesses (compete with big chains)
- Generates data and sponsorship opportunities

---

## 23. TRAVEL MODE

### Concept (Future Feature)
- Location-aware mobile experience
- Detects when user is traveling through a new community
- Provides real-time recommendations: restaurants, attractions, gas, events
- Audio responses for hands-free use while driving

---

## 24. COMMUNITY CHAT

### Purpose
- Local discussion forum / real-time conversation
- Community interaction (not AI chat — human-to-human)
- Social layer of the platform

### Moderation Strategy
- AI moderation for toxic content
- Structured engagement (topics, channels) to reduce noise
- Community guidelines enforced by publisher

---

## 25. NAMING & DOMAIN STRATEGY

### Working Name: Popular Network

### Naming Goals
- Short, memorable, unique
- AI-forward / modern feeling
- Brandable with available .com domain

### Explored Directions
- Historical: Agora, Forum
- Latin roots: Conexus, Nexa
- Abstract: Nexilo, Aetherix
- Conceptual: Weave, Mesh

### Domain Strategy
- Many obvious domains are taken
- Approach: invent new words, combine roots, focus on brandability
- Must secure .com

### Status: Not finalized — building under working title for now

---

## 26. RISKS & MITIGATIONS

| Risk | Mitigation |
|------|-----------|
| Toxic community chat | AI moderation + structured engagement + publisher oversight |
| Feature fragmentation | Unified platform under single UX; strict category hierarchy |
| Scope creep | Phased build plan; MVP-first approach |
| Publisher content delivery | Define clear input requirements and formats upfront |
| Competing with publisher core products | Platform complements, not replaces, existing newspaper business |
| Data ownership / scraping legality | Use official APIs where possible; clear ToS for scraped data |
| Time constraints of founders | All have existing roles; need focused sprint planning |
| Multi-tenancy complexity | Architect for multi-tenant from Day 1 |
| LLM costs at scale | Cache common queries; optimize token usage; estimate costs per user |
| Hallucination / bad AI answers | RAG grounding with local data; human review for published content |

---

## 27. KNOWN GAPS & OPEN QUESTIONS

These items have been identified but NOT resolved across the 11 conversations:

1. **Pricing:** Territory licensing price, business subscription tiers, consumer subscription price — none finalized
2. **Content operations playbook:** Who uploads what, how often, in what format — not documented
3. **Onboarding workflow details:** Step-by-step process for new publishers joining the network
4. **Governance structure:** Founder equity, vesting, decision-making — discussed but not decided
5. **Legal entity:** Must be separate company from Quadd — not yet formed
6. **Product packaging:** Core product vs. add-ons, bundling strategy, upgrade paths — not defined
7. **Customer segmentation:** Beyond publishers — advertisers, agencies, local businesses, other content creators
8. **Platform vs. decentralization balance:** How much control stays local vs. centralized
9. **Feedback collection system:** How pilot users provide structured feedback
10. **Support infrastructure:** How publishers get help when things break

---

## 28. PHASED BUILD PLAN

### PHASE 1 — MVP / Pilot (0–60 Days)
**Goal:** Working product for Southwest Peach pilot group

Build:
- [ ] Multi-tenant database schema (PostgreSQL)
- [ ] Publisher admin dashboard (basic)
  - [ ] Content management (add/edit/delete articles, events, businesses)
  - [ ] Business directory management
- [ ] AI chat interface (web-based)
  - [ ] Natural language input
  - [ ] RAG-powered responses using local data
  - [ ] Hybrid output: text summary + structured cards
- [ ] Business directory
  - [ ] Searchable by category, location, name
  - [ ] Basic listings (name, address, phone, hours, description)
  - [ ] Google Places API backfill for initial data
- [ ] News article display
  - [ ] Article list/feed view
  - [ ] Individual article pages
  - [ ] Category filtering (news, sports, opinion, obituaries)
- [ ] Events calendar
  - [ ] List and calendar views
  - [ ] Add/edit events (publisher admin)
  - [ ] Searchable by date, category
- [ ] Weather integration
  - [ ] OpenWeather API per location
  - [ ] Display on homepage and in chat responses
- [ ] Homepage with layered architecture
  - [ ] Trust layer (logo, nav, featured story)
  - [ ] AI discovery layer (chat prompt, suggested queries)
  - [ ] Content layer (news feed)
- [ ] Basic data ingestion pipeline
  - [ ] Manual article entry
  - [ ] Google Places API business import
  - [ ] Event entry (manual)
- [ ] User-facing web app (responsive)
- [ ] Vector store (ChromaDB) loaded with all content for RAG

### PHASE 2 — Revenue & Business Tools (60–120 Days)
**Goal:** Enable monetization and business participation

Build:
- [ ] Business subscription system
  - [ ] Stripe integration for payments
  - [ ] Tier management (free, basic, premium)
- [ ] Paid business placements
  - [ ] Featured listings in AI responses
  - [ ] Homepage featured business module
  - [ ] "Recommended by..." sponsored results
- [ ] Business onboarding flow
  - [ ] Publisher enters business name → auto-fill from APIs
  - [ ] Onboarding email sent to business
  - [ ] Business claims and enhances listing
- [ ] Social media aggregation
  - [ ] Facebook page content sync
  - [ ] Instagram feed sync
  - [ ] Display social content on business profiles
- [ ] Business profile pages
  - [ ] Full listing with social feed, reviews, hours, contact
  - [ ] Individual business chatbot (answers questions from listing data)
- [ ] Classifieds module
  - [ ] User submission form
  - [ ] Categories, photos, pricing
  - [ ] Expiration dates
- [ ] Job listings module
  - [ ] Radius-based search
  - [ ] Category filtering
- [ ] Ad management system (publisher admin)
  - [ ] Create/manage ad placements
  - [ ] Basic impression/click tracking
- [ ] Analytics dashboard (publisher)
  - [ ] Traffic, engagement, top queries
  - [ ] Business listing performance
- [ ] Dynamic landing pages
  - [ ] Auto-generated from AI queries
  - [ ] Include relevant businesses, specials, ads

### PHASE 3 — AI Content & Community (120–180 Days)
**Goal:** Automate content creation and build community engagement

Build:
- [ ] AI content generation pipeline
  - [ ] Press release → article
  - [ ] Meeting minutes → summary
  - [ ] Audio upload → transcription + article
  - [ ] Sports stats → recap
- [ ] Editorial review queue
  - [ ] AI drafts flagged for human review
  - [ ] Approve / edit / reject workflow
- [ ] Community chat
  - [ ] Topic-based channels
  - [ ] AI moderation layer
  - [ ] Community guidelines enforcement
- [ ] Polls and engagement tools
- [ ] Youth sports module
  - [ ] Parent/coach data upload form
  - [ ] AI-generated game recaps
- [ ] Personalized alerts
  - [ ] Follow businesses, categories, topics
  - [ ] Push notifications or email
- [ ] User accounts and preferences
  - [ ] Registration / login
  - [ ] Saved searches, followed businesses
  - [ ] Location preferences
- [ ] Consumer premium subscription tier
  - [ ] Paywall for full articles (vs AI summary)
  - [ ] Ad-free option
  - [ ] Exclusive content access

### PHASE 4 — Network & Scale (180–365 Days)
**Goal:** Expand beyond pilot, enable network features

Build:
- [ ] Multi-publisher network infrastructure
  - [ ] Shared job listings across territories
  - [ ] Shared classified listings (radius-based)
  - [ ] Cross-publisher content sharing
- [ ] National advertising system
  - [ ] Reserved ad slots across all publishers
  - [ ] Sponsored AI responses
  - [ ] Network-wide campaign management
- [ ] Publisher onboarding system
  - [ ] Self-service territory signup
  - [ ] Automated data backfill for new territory
  - [ ] Template branding setup
- [ ] Real estate listings module
  - [ ] MLS integration or manual entry
  - [ ] Search, filter, map view
- [ ] Vehicle listings module
  - [ ] Dealer inventory sync (CRM scraping)
  - [ ] Private seller submissions
- [ ] Rewards / loyalty system
  - [ ] QR-based redemption
  - [ ] Business enrollment
  - [ ] Points tracking
- [ ] Advanced analytics
  - [ ] Reader behavior insights
  - [ ] Ad performance tracking
  - [ ] Predictive recommendations
- [ ] Mobile app (native or PWA)
- [ ] Travel mode (location-aware, audio responses)

### PHASE 5 — Advanced Features (12+ Months)
- [ ] AI camera sports streaming integration
- [ ] Live scoring + auto-highlights
- [ ] Podcast hosting and distribution
- [ ] Video content platform
- [ ] Games (crosswords, trivia, contests)
- [ ] Leaderboards
- [ ] Government meeting recording + AI processing
- [ ] Advanced CRM / inventory syncing for businesses
- [ ] Business dashboard with AI insights and budget allocation

---

## 29. MVP DEFINITION (PHASE 1)

To be absolutely clear, the MVP for the Southwest Peach pilot is:

### Must Have
1. AI chat interface that answers natural language questions
2. Business directory (populated via Google Places API)
3. News articles (manually entered or imported)
4. Events calendar
5. Weather widget
6. Homepage with AI discovery layer as the primary interaction
7. Publisher admin dashboard for content management
8. Multi-tenant architecture (supports multiple publishers/territories)
9. RAG pipeline (ChromaDB) indexing all content for AI search
10. Responsive web design (works on mobile browsers)

### Must NOT Have (Phase 1)
- Payment processing
- User accounts / login
- Business onboarding self-service
- Social media syncing
- AI content generation
- Community chat
- Classifieds / jobs / real estate
- Mobile app
- Rewards system
- National ad network

---

## 30. DATABASE SCHEMA (STARTING POINT)

See Section 11 for full table definitions. For Phase 1 MVP, implement these tables first:

1. `publishers` — territory and branding
2. `businesses` — directory listings
3. `news_articles` — content
4. `events` — calendar
5. `weather_cache` — cached weather data
6. `chat_sessions` — conversation logs
7. `locations` — evergreen local data (schools, churches, govt)

Add in Phase 2:
- `users`
- `ads`
- `classifieds`
- `job_listings`
- `social_posts`

Add in Phase 3+:
- `real_estate_listings`
- `vehicle_listings`
- Rewards/loyalty tables
- Analytics/tracking tables

---

## 31. FILE & FOLDER STRUCTURE (SUGGESTED)

```
popular-network/
├── README.md
├── docker-compose.yml
├── .env.example
│
├── backend/
│   ├── api/
│   │   ├── routes/
│   │   │   ├── chat.py          # AI chat endpoint
│   │   │   ├── articles.py      # News CRUD
│   │   │   ├── businesses.py    # Business directory CRUD
│   │   │   ├── events.py        # Events CRUD
│   │   │   ├── weather.py       # Weather proxy
│   │   │   └── admin.py         # Publisher admin endpoints
│   │   └── middleware/
│   │       └── tenant.py        # Multi-tenant context
│   │
│   ├── services/
│   │   ├── llm.py               # LLM integration (OpenAI/Claude)
│   │   ├── rag.py               # RAG pipeline (ChromaDB)
│   │   ├── ingestion.py         # Data ingestion service
│   │   ├── google_places.py     # Google Places API client
│   │   ├── weather.py           # OpenWeather API client
│   │   └── scraper.py           # Web scraping service
│   │
│   ├── models/
│   │   ├── publisher.py
│   │   ├── business.py
│   │   ├── article.py
│   │   ├── event.py
│   │   ├── location.py
│   │   ├── chat_session.py
│   │   └── weather_cache.py
│   │
│   ├── database/
│   │   ├── connection.py
│   │   └── migrations/
│   │
│   └── config/
│       └── settings.py
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── ChatInterface/    # Main AI chat
│   │   │   ├── BusinessCard/     # Business listing card
│   │   │   ├── EventCard/        # Event display card
│   │   │   ├── ArticleCard/      # News article card
│   │   │   ├── WeatherWidget/    # Weather display
│   │   │   ├── Homepage/         # Homepage layout
│   │   │   └── Navigation/       # Top nav bar
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── BusinessDirectory.jsx
│   │   │   ├── EventsCalendar.jsx
│   │   │   ├── ArticlePage.jsx
│   │   │   └── BusinessProfile.jsx
│   │   ├── admin/
│   │   │   ├── Dashboard.jsx
│   │   │   ├── ArticleManager.jsx
│   │   │   ├── BusinessManager.jsx
│   │   │   └── EventManager.jsx
│   │   └── services/
│   │       └── api.js            # API client
│   └── package.json
│
├── vectorstore/
│   ├── indexer.py                # Index content into ChromaDB
│   └── config.py
│
├── scripts/
│   ├── seed_businesses.py        # Google Places API backfill
│   ├── seed_locations.py         # Load evergreen data
│   └── import_articles.py        # Bulk article import
│
└── docs/
    ├── PROJECT_SPEC.md           # This file
    ├── API.md                    # API documentation
    └── DEPLOYMENT.md             # Deployment guide
```

---

## END OF SPECIFICATION

This document represents the consolidated knowledge from 11 strategic conversations about the Popular Network project. It should be treated as the single source of truth for project scope, architecture, features, and phasing.

**For Homer:** Start with Phase 1 (MVP). Build the database schema, the AI chat interface with RAG, the business directory with Google Places backfill, the news/events modules, the weather integration, and the homepage layout. Everything else comes later.

**Priority order within Phase 1:**
1. Database schema + multi-tenant setup
2. Backend API scaffolding
3. Google Places business backfill script
4. RAG pipeline (ChromaDB indexing)
5. AI chat endpoint (LLM + RAG)
6. Frontend homepage with chat interface
7. Business directory pages
8. News article pages
9. Events calendar
10. Weather widget
11. Publisher admin dashboard
12. Connect everything to the homepage AI layer
