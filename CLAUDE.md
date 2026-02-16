# Toolkit AI Website — Claude Code Instructions

## What This Project Is

Single-page marketing website for Toolkit AI — an AI automation consulting business for trades (plumbers, electricians, HVAC, contractors, landscapers) in Southern Alberta and Interior BC. Co-founded by Devyn and Brian.

**Live URL:** [will be set once Vercel is connected]
**Repo:** toolkit-ai-site
**Deploy:** Vercel auto-deploy on push to main

## Working With Devyn

- Has ADHD. Break tasks into clear steps. Don't dump everything at once.
- If a task has more than 3 steps, number them and pause for confirmation between major phases.
- Be direct. Push back if something won't work.
- Technical enough to follow along but still learning. Don't over-explain basics, don't assume deep expertise.

## Pre-Flight Check (ALWAYS)

Before starting any task that involves multiple files or more than 5 minutes of work:
1. Restate what you think I'm asking for in one sentence
2. Break the task into numbered sub-tasks
3. Flag anything complex enough to be its own session
4. Confirm the plan before starting

If I say "just go" or "skip the plan," proceed. Always default to planning first.

---

## Technical Stack

- **Plain HTML/CSS/JS** — no framework. Single file to start, split into separate CSS/JS files when it gets unwieldy.
- **Hosting:** Vercel (GitHub auto-deploy)
- **Animation:** CSS animations + vanilla JS (Intersection Observer for scroll triggers). GSAP only if CSS can't achieve the effect.
- **Icons:** Lucide or Heroicons (CDN)
- **Font:** Single Google Font family — Manrope, Inter, DM Sans, or similar. Use weight variations for hierarchy.
- **CTA Integration:** Cal.com (free tier) for booking links
- **Device Mockups:** Pure CSS iPhone/laptop frames
- **Responsive:** Mobile-first. Design for 375px width first, then scale up. Tradespeople are on phones.

---

## Design System

### Colors (Grounded & Practical — Not Tech SaaS)

- **Page background:** Warm off-white — `#FAFAF7` or `#F8F7F4`. Paper-like, not stark.
- **Primary text:** Deep charcoal with warmth — `#1A2B33` or `#2C3E50`. Not pure black.
- **Body text:** Primary at 70-80% opacity.
- **Primary CTA:** Confident, trustworthy blue-green — in the `#2563EB` to `#1D7A6A` range. Pops against warm background.
- **Accent/highlight:** Warm amber/gold for section labels — `#D4940A` to `#F0B429` range.
- **Card backgrounds:** White or slight blue-tint (`#F0F4F8`).
- **Borders:** Never harsh. `rgba(0,0,0,0.06)` to `rgba(0,0,0,0.10)` max. Separation through whitespace first.

**NOTE:** Propose 2-3 specific palettes for Devyn's approval before building. One trustworthy blue-green, one warmer/earthier, one bolder.

### Typography

Single font family. Weight variations for hierarchy:

- **Hero headline:** 56-64px, weight 700, line-height 1.1
- **Section headings:** 40-48px, weight 700
- **Sub-headings:** 24-28px, weight 600
- **Body text:** 16-18px, weight 400-500, line-height 1.6
- **Small text/labels:** 14px, weight 500
- **Section labels** (e.g. "THE PROBLEM"): 14px, weight 500, uppercase, amber/gold gradient text via `background-clip: text`

### Spacing & Layout

Generous whitespace = premium feel:

- **Between major sections:** 100-140px
- **Section internal padding:** 60-80px top and bottom
- **Max content width:** 1200px centered
- **Split layout sections** (text + demo): 45/55 split on desktop, stack on mobile
- **No divider lines.** Separation = whitespace + subtle background color shifts.
- **Card border-radius:** 12-16px consistently
- **Card padding:** 24-32px internal
- **Borders:** No hard borders. Cards use `1px solid rgba(0,0,0,0.08)` or no border with subtle shadow.
- **Buttons:** 12px border-radius

---

## The Two Audiences

**Audience 1: Skeptical Tradespeople**
- Late adopters, confused by AI, trust local over corporate
- Care about: missed calls, booked estimates, saving time, getting more reviews, NOT writing emails
- Do NOT care about: n8n, MCP, agents, APIs, automation architecture
- Language: plain English, outcome-focused
- The demos sell this audience — seeing is believing

**Audience 2: Brian (Co-founder)**
- Head of Sales at Alteryx Canada — knows SaaS, knows scale
- Needs to see: professional presentation, scalable business, market opportunity
- The site quality itself is a signal

## Brand Voice

- Approachable, not slick
- Knowledgeable, not jargon-heavy
- Confident, not salesy
- Every claim needs an outcome: never "we build AI agents" → always "we cut your missed calls by 80%"
- OK to be slightly cheeky/human
- Two emotional hooks: (1) stop losing money (logical) and (2) stop doing the shit you hate — emails, customer chasing, admin (emotional/freedom)

---

## Competitive Positioning (Use in Copy)

**We are NOT field service management software.** We don't compete with Jobber, ServiceTitan, Housecall Pro. We plug into the gaps between those tools.

- "Works alongside your Jobber" (not "replaces Jobber")
- "Plugs into your existing QuickBooks" (not "switch to our system")
- "You don't need to learn another app. You don't even need to change your phone number."

**Key stats for copy (all real, from market research):**
- Most 1-5 person crews spend $0-$80/mo on software total
- Owner-operators miss 30-50% of calls while on job sites
- 67% of customers prefer SMS for scheduling; 98% of texts read within 3 minutes
- Average trades business has fewer than 30 Google reviews
- Consumers read ~10 reviews before trusting a local business
- Profiles with photos get 42% more direction requests
- Recovering 3-5 missed calls/month = $900-$4,000 in recovered revenue vs $100-$300/mo cost = 3x-15x ROI

**Tools our audience actually uses (name-drop these):**
- **Jobber** — default FSM in Western Canada (Edmonton-founded)
- **QuickBooks** — 62% of Canadian SMBs
- **Google Business Profile** — 50%+ of contractor leads
- **HomeStars** — THE Canadian lead gen platform (~8M homeowners)
- **Square** — dominant payment processor for small trades
- **Personal cell phone** — this IS the business phone for most

---

## Page Structure — Section by Section

### Section 1: HERO

**Layout:** Centered single-column.

**Content stack:**
1. Trust badge pill (placeholder: "Built for trades in Western Canada")
2. Main headline: 56-64px bold. Speaks to pain AND aspiration. Write real copy.
3. Subtitle: 16-18px, 80% opacity, 2 lines max. Plain English.
4. Primary CTA: "Book Your Free AI Audit" — filled button
5. Below CTA: "15 minutes. No commitment. We show you exactly where AI saves you time."
6. Secondary: "See it in action ↓" — scroll anchor to demo section

**Hero visual:** CSS-built iPhone frame with animated sequence inside. Auto-plays on load.

**Hero animation (linear, plays once, ~12-15s):**
1. iPhone shows incoming call: "Sarah Mitchell — Missed Call" (1.5s)
2. AI texts Sarah: "Hi Sarah, thanks for calling [Business]. Sorry we missed you — how can we help?" (typing indicator 0.8s → message 2s)
3. Sarah: "My kitchen faucet is leaking pretty bad" (1.5s)
4. AI: "That sounds urgent. I can get Mike out tomorrow morning between 8-10 AM — does that work?" (2s)
5. Sarah: "Yes perfect" (1s)
6. AI: "You're all set! Mike will see you tomorrow at 8 AM. You'll get a confirmation text shortly. 👍" (2s)
7. Split/second phone shows Mike receiving: "New booking: Sarah Mitchell, 123 Main St, kitchen faucet leak, tomorrow 8-10 AM" (2s)

Optional: Subtle floating tool icons around phone (Jobber, Google, phone) connected by thin curved lines.

---

### Section 2: THE PROBLEM

**Layout:** Centered, stacked.

**Content:**
1. Gold label: "THE PROBLEM"
2. Heading: ~48px bold. About losing money when phone rings unanswered.
3. Body: 1-2 sentences
4. Three stat cards in a row (stack on mobile):
   - "30-50%" → "Of calls missed while you're on a job site"
   - "$900-$4,000" → "In revenue lost every month to missed calls alone"
   - "10 reviews" → "What customers read before they trust you — how many do you have?"
5. Transition: "What if you never missed another call?" with downward arrow

**Stat card styling:** Amber/warm gradient text for numbers via `background-clip: text`. Light warm tint background. Rounded corners, generous padding.

**Messaging hits both angles:**
- Money: "You're losing $900-$4,000/month and you don't even know it"
- Freedom: "You didn't get into [trade] to spend your evenings writing emails and chasing customers"

---

### Section 3: INTERACTIVE DEMOS — TIER 1 (PRO)

**Section intro:**
- Gold label: "SEE IT WORK"
- Heading: "Manage the work you already have"
- Subtitle: About stopping lost jobs and running smoother

**Layout:** Alternating split sections — text left/demo right, then demo left/text right. Each demo is its own section with generous spacing.

**Animation behavior:** Linear sequence triggered by Intersection Observer when 30% visible. Plays ONCE. Small "↻ Replay" button in corner. Each sequence 10-15s. Timing per message: 1.5-2.5s. Typing indicators 0.8-1s before AI messages. Smooth fade/slide transitions.

#### Demo 1: AI Phone Receptionist
**Text side:** "Every call answered. Every lead captured." — about how AI answers when you're on a job site, books the job, texts you details.

**Demo (iPhone mockup):**
1. Incoming call: "Unknown Number" with Accept button
2. AI answers with voice waveform: "Hi, you've reached [Business]. How can I help?"
3. Caller: "My furnace stopped working and it's freezing in here"
4. AI: "I'm sorry to hear that. Let me get a technician out. Are you available tomorrow between 8 and noon?"
5. Caller: "Tomorrow morning works"
6. AI: "Perfect. I've booked you in. You'll receive a confirmation text."
7. Transition to outgoing text to "Mike (Owner)": "🔔 New booking: Furnace repair, 742 Oak Street, tomorrow 8-12 PM"

#### Demo 2: Smart Estimate Follow-Up
**Text side (RIGHT — alternating):** "Quotes that don't go cold." — about following up at the right time so you don't have to.

**Demo (LEFT, text message mockup):**
1. AI texts Dave: "Hi Dave, just checking in on the estimate for your deck repairs. Any questions?"
2. "Dave is typing..." (2s)
3. Dave: "Is the price firm or is there any flexibility?"
4. AI: "Great question. Let me check with Mike and get right back to you."
5. AI: "Mike says he can take 10% off if you book this week. Want me to get you on the schedule?"
6. Dave: "Yeah let's do it. Thursday work?"
7. AI: "Thursday it is! You'll get a confirmation shortly. Thanks Dave 👍"
8. Badge overlay: "💰 $2,400 job saved from going cold"

#### Demo 3: Automated Review Collection
**Text side (LEFT):** "5-star reviews on autopilot." — friendly text after every job, no awkward asking.

**Demo (RIGHT, two-phase):**
Phase 1 — Text: AI sends review request → Sarah replies "Mike was great! Done ✅"
Phase 2 — GBP mockup: Sarah's 5-star review appears on a Google Business Profile card. Counter ticks 47→48 reviews. Stat: "Avg client: 12 new reviews in first 60 days"

#### Demo 4: Morning Briefing
**Text side (RIGHT):** "Start every day in control." — before your first coffee, you know your whole day.

**Demo (LEFT, text message):** Typing indicator → message fades in line by line:
```
☀️ Good morning, Mike. Here's your Tuesday:

📋 SCHEDULE
• 3 jobs booked in Jobber today
• First call: 8 AM — Sarah Mitchell, kitchen faucet

💰 FOLLOW-UPS
• 2 estimates pending — one going cold (Dave's deck, 3 days ago)
• 1 new lead overnight from Google Business Profile

⭐ REVIEWS
• New 5-star review from Jennifer T. — want me to reply?
• Your Google rating: 4.8 (48 reviews)

Reply 1️⃣ 2️⃣ or 3️⃣ to take action
```

---

### Section 3B: DEMOS — TIER 2 (MAX)

**Transition:** "Now that you're running smooth..." → "Everything above PLUS the tools that grow your business."

- Gold label: "GO FURTHER"
- Heading: "Grow the work coming in"

#### Demo 5: GBP Optimization
GBP card transforming: sparse "before" (2 photos, 12 reviews) → animated optimization → complete "after" (40+ photos, 48 reviews). Stat: "Profiles with photos get 42% more direction requests"

#### Demo 6: Website & Online Presence
Laptop frame: professional trades website assembling section by section, mobile preview beside it, Google search result appearing. Stat: "Your 24/7 digital storefront"

**Max demos are simpler/shorter than Pro demos.** Pro is the money section. Max is the upsell.

---

### Section 4: HOW IT WORKS

Three cards in a row, numbered 1-2-3:

1. **"Free AI Audit"** — 15-min call, we look at your setup, show where you're losing time/money. No sales pitch.
2. **"We Build Your Toolkit"** — Custom to your business, plugs into existing phone/texts/tools. No new app to learn.
3. **"You Do Your Trade"** — Calls answered, quotes followed up, reviews come in. You do the work you started your business to do.

Card styling: 12-16px radius, illustration area top 60% with light blue tint, text below.

---

### Section 5: WHO WE ARE

Short and personal. Not corporate.

- Heading about two guys in Western Canada bringing AI to trades
- 3-4 sentences: Devyn (sales/tech) + Brian (Head of Sales, Alteryx Canada). Saw AI helping big companies, nobody bringing it to trades.
- Photo placeholders (circles)
- Locations: Lethbridge, AB + Cranbrook, BC
- Trust: "We use the same AI tools we set up for your business."

---

### Section 6: PRICING

Three cards:

#### "The Apprentice" (Cheeky Comparison)
- Title: "The Apprentice" / Subtitle: "Straight out of trade school"
- Price: "$3,500/month" (crossed out)
- Satirical features:
  - "Spends more time on TikTok than threading pipe"
  - "Shows up 20 minutes late with a Tim Hortons coffee"
  - "Asks 'what do you want me to do now?' every 11 minutes"
  - "Loses your best crescent wrench on day one"
  - "Calls in sick on Mondays after the Flames game"
  - "Needs supervision, a pep talk, and a ride home"
- No CTA. Warm humor — not cruel. Every journeyman has been there.

#### "Pro" (Highlighted — amber border glow)
- Subtitle: "Manage the work you already have"
- Price: "$297-$497/month"
- Features: AI phone receptionist 24/7, smart follow-ups, review collection, morning briefings, works with Jobber/QuickBooks/GBP, no more writing follow-up emails
- CTA: "Book Your Free Audit" — filled button, full width
- Below: "Includes free AI audit + custom setup"

#### "Max"
- Subtitle: "Grow the work coming in"
- Price: "$997-$1,497/month"
- Features: Everything in Pro + website, GBP optimization, local SEO, monthly reporting, priority support
- CTA: "Book Your Free Audit" — outline button

---

### Section 7: TESTIMONIALS

**7A: Featured testimonial** — large card, light background, big quotation mark, 20-22px text. Placeholder: realistic copy + "Mike R., R&M Plumbing, Lethbridge"

**7B: Results stat bar** — 3-4 big numbers with count-up animation: calls answered, estimates booked, reviews collected. Placeholder numbers.

---

### Section 8: FAQ

Accordion-style. Full-width cards, plus/minus icon, smooth expand. Questions:

1. "How is this different from Jobber / ServiceTitan?" → We work alongside them. Jobber manages jobs. We catch the calls that create jobs.
2. "What if my customers hate talking to a robot?" → They won't know. And right now they're talking to your voicemail. That's worse.
3. "I'm not tech savvy — is this complicated?" → No new app. Plugs into existing phone/texts/tools.
4. "How long does setup take?" → Most live within a week. Audit is 15 minutes.
5. "Do I need to change my phone number?" → No.
6. "What if I want to cancel?" → Month to month. No contracts.
7. "How much does it actually cost?" → Pro from $297/mo. Recovering 3 missed calls pays for it.
8. "Can I try before I commit?" → Free audit. No commitment.

---

### Section 9: FINAL CTA

Warm gradient background (off-white → soft peach/amber).
- Heading: "Your trade. Our toolkit." — hand-drawn golden underline squiggle on "toolkit" (SVG/CSS)
- Body: about stopping lost calls, chasing customers, writing emails. Book audit, 15 minutes.
- CTA: "Book Your Free AI Audit" — large, filled, centered
- Below: "Or text us at [phone number] — we practice what we preach."

---

### Section 10: FOOTER

- Left: Logo, "Your trade. Our toolkit.", Lethbridge AB + Cranbrook BC
- Services: AI Phone Receptionist, Smart Follow-Ups, Review Collection, Morning Briefings, Website & SEO
- Company: About, Pricing, FAQ, Contact, Free AI Audit
- Connect: Email, phone, social links
- Bottom: "© 2026 Toolkit AI. Built with AI in Western Canada."

---

## Animation Spec Summary

| Element | Trigger | Behavior | Duration |
|---------|---------|----------|----------|
| Hero phone demo | Page load | Linear, plays once | 12-15s |
| Stat numbers | Scroll into view | Count-up | 1.5-2s |
| Pro demos (1-4) | Scroll 30% visible | Linear, plays once, replay button | 10-15s each |
| Max demos (5-6) | Scroll 30% visible | Single transformation | 5-8s each |
| Section reveals | Scroll into view | Fade-up, 20-30px offset | 0.4-0.6s |
| FAQ accordion | Click | Height expand/collapse | 0.3s |
| Logo marquee | Always | Horizontal scroll | Infinite |
| CTA buttons | Hover | Scale 1.02 + color shift | 0.2s |

**Easing:** `cubic-bezier(0.22, 1, 0.36, 1)` — smooth, natural

---

## Build Order

1. **Hero + Demo 1 (AI Phone Receptionist) FIRST.** Show Devyn before building anything else. If this doesn't hit the bar, nothing else matters.
2. Section 2 (Problem) + Section 3 remaining demos
3. Section 3B (Max demos)
4. Sections 4-5 (How It Works, Who We Are)
5. Section 6 (Pricing with Apprentice card)
6. Sections 7-10 (Testimonials, FAQ, Final CTA, Footer)

## What NOT To Do

- Don't try to fetch or browse any URLs
- Don't use lorem ipsum — write real draft copy
- Don't build the blog, SEO automation, or backend integrations
- Don't use a framework — plain HTML/CSS/JS
- Don't treat demos as a polish step — they ARE the site
- Don't settle for "good enough" on animations — this is the core selling tool
