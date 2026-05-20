# TikTok Publisher

> **Agent**: `depositback-agent-tiktok-publisher`  
> **Group**: Distribution  
> **Product**: DepositBack — Security Deposit Demand Letter Service

## Purpose

Schedules and publishes text-on-screen explainers, Duets, and educational shorts. Targets 60+ videos in 90-day sprint with 3.7%+ engagement.

## DepositBack Context

DepositBack is a single-page, no-signup transactional product for US renters seeking to recover security deposits. The entire customer journey fits on one URL: landing page → 6-question form → Revolut payment → PDF emailed. Conversion rate target: **4% visitor-to-purchase minimum**.

## Inputs

- TikTok scripts from social-content-creator
- State law snippets from geo-content-generator

## Outputs

- Published TikTok URLs → analytics/funnel-analyst inbox

## Human Escalation Points 🛑

- Content flagged by platform
- Copyright/music licensing issues
- Crisis response posts

## Skills

| Skill | Description | Status |
|-------|-------------|--------|
| `noop` | Health check / pipeline verification | ✅ Active |
| `execute` | Primary function for this agent | 🔧 Planned |

## Workflow

1. Poll `data/inbox/` for task manifests from upstream agents.
2. Resolve required skills (local `skills/` or ClawHub fallback).
3. Execute workflow.
4. Write artifacts to `data/outbox/`.
5. Update `data/state.json`.

## Runtime

```bash
pip install -r requirements.txt
python runtime/main.py
```
