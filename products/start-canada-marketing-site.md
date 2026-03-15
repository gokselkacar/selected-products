# START Canada Marketing Site

Production marketing website for START Canada.

## Live Product

- Website: [startnew.ca](https://startnew.ca/)

## Summary

START Canada Marketing Site is a Next.js platform designed to present employability assessments, career bootcamps, and certification programs through a modern, responsive experience.

## Product Scope

- Public-facing marketing website for START Canada's programs and brand story.
- Multi-page experience covering products, gallery content, contact flows, and policy pages.
- Content-oriented platform built to support program discovery and lead generation.

## User Experience

- Home page with hero messaging, proof points, audience targeting, and product positioning.
- Projects page with structured navigation across employability score, bootcamp, and certification offerings.
- Gallery experience with category filters and lightbox interactions.
- Contact journey with purpose-based routing and support / newsletter flows.

## My Contribution

- Built and structured the application using the Next.js App Router and TypeScript.
- Implemented reusable UI components, responsive navigation, and branded presentation layers.
- Added contact, newsletter, support, and health API routes with validation and rate limiting.
- Supported content publishing through MDX and gallery manifests.

## Stack

- Next.js
- React
- TypeScript
- TailwindCSS
- Zod
- Nodemailer
- Playwright
- Docker

## Product Capabilities

- Responsive navigation with desktop and mobile-specific interaction patterns.
- File-based blog and gallery content workflows for easier ongoing updates.
- Contact, newsletter, and support submission flows with validation and abuse protection.
- Placeholder-aware image system designed to allow staged content rollout without broken layouts.

## Architecture Overview

- Next.js App Router frontend with reusable component-driven page structure.
- Lightweight API route layer for contact, newsletter, support, and health endpoints.
- File-based content management using MDX and JSON manifests instead of a CMS dependency.
- Docker and Nginx-ready deployment setup for consistent production delivery.

## Highlights

- Multi-page marketing experience with projects, gallery, contact, privacy, and terms pages.
- Form handling with validation, sanitization, honeypot checks, and rate limiting.
- File-based content workflows for blog and gallery management.
- Production-oriented deployment setup with Docker and Nginx support.

## Delivery Notes

- Built with a strong emphasis on responsiveness, accessibility, and maintainable content updates.
- Structured to support staged media rollout with placeholders before final brand assets are published.
- Designed to operate as both a marketing layer and a reliable lead capture surface.

## Repository Note

The source code for this product is maintained in a private repository. This page is a public product summary.
