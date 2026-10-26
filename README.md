Portal — Geospatial Data Delivery Platform (Case Study)

> **Note:** Portal is a commercial, closed-source product owned by The Scan Station.
> This repository is a **public case study** — architecture, scale and results only.
> No proprietary source code is included.

**Role:** Sole architect & developer · **Live product:** site-portal.co.uk

---

## The problem

Drone and LiDAR surveys of large industrial assets produce **500GB+ datasets** — 3D point
clouds, 360° imagery, orthophotos. Clients' machines couldn't open them, and sending data around
engineering teams by hard drive was slow, insecure and unscalable.

## What I built

A secure, serverless web platform that lets clients view and distribute massive geospatial
datasets straight from the browser — interactive 3D point clouds, 360° panoramas, orthophotos,
asset/pipeline overlays, and live drone streaming.

I owned the whole thing solo: product discovery with clients, architecture, frontend, backend,
cloud infrastructure, data pipelines and deployment.

## Architecture

- **Full-stack:** Next.js (JavaScript) — server and client in one framework, with in-browser
  3D point-cloud and 360° viewers
- **Data:** MongoDB (schema re-designed via Python driver migration to kill anti-patterns and
  speed up queries on large object lists)
- **Cloud / hosting:** AWS Amplify with CloudFront CDN distributions; S3 storage with automated
  lifecycle tiering to cold storage
- **Processing:** a Windows-Docker pipeline wrapping the Reality Scan (formerly RealityCapture)
  CLI, splitting photogrammetry across cost-optimised AWS compute tiers (memory-optimised for
  image alignment, GPU-optimised for reconstruction)
- **Delivery:** CI/CD, AI-augmented development, Agile sprints driven by direct client feedback

## Results

| Outcome | Impact |
|---|---|
| Platform adoption | **6,000+ engineers**, now written into client contracts as a delivery requirement |
| Project scale supported | **£5bn+** of infrastructure (Palace of Westminster, Essar Stanlow, Grangemouth, Basra oil & gas) |
| Commercial impact | Revenue unlocked **tripled the team and multiplied EBITDA** |
| Orthophoto automation | removed **~20 hrs/week** of manual work |
| Survey-pipeline automation | saved **~56 engineer-hours/week** |
| Cloud cost | cut **~£3,500/month** via S3 tiering |
| New revenue stream | photogrammetry-as-a-service pipeline (Reality Scan CLI) |

## The hybrid edge

A pure software engineer couldn't have built this — it needed someone fluent in both the survey
domain and the code. Background: BSc (Hons) Music Technology (First), PG Diploma in Acoustics,
then self-taught to shipping a commercial platform solo.
