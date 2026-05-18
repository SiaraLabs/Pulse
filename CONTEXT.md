# Pulse — Project Context

## What we're building
A minimal SaaS analytics dashboard. Stripe-connected. Four metrics only.
No session replay. No AI features. No tiers. €34.99/mo.

## The four metrics
1. Where paying customers came from (UTM → Stripe customer attribution)
2. Trial to paid conversion % this month
3. Landing page views (first-party tracking)
4. Weekly revenue cohorts

## Stack
- Next.js (frontend + API routes)
- Stripe API (read-only key, webhooks)
- Postgres (Supabase to start)
- Deployed on Hetzner

## Current structure
- /landing — landing page with email waitlist capture
- /dashboard — the actual product (not started yet)
- /api/stripe — webhook handler (not started yet)
- /api/attribution — UTM capture endpoint (not started yet)

## Key decisions made
- Read-only Stripe API keys only, never write access
- UTM data written directly into Stripe customer metadata
- First-party tracking script, no Google Analytics dependency
- Single plan, no free trial, email waitlist until launch

## Known hard problems
- MRR calculation edge cases: refunds, upgrades, pauses, lifetime deals
- Attribution breaks when signup is through Clerk or Auth0
- Need to carry UTMs through redirect URL as fallback

## What's done
- Landing page in progress (hero animation resolved)
- Email waitlist capture UI built
- Repo initialized with README, CONTEXT, DEVLOG

## What's next
- Polish and ship landing page
- Post on Reddit (day 1 building in public)
- Set up Stripe webhook endpoint
- Build UTM capture script
- Start dashboard UI