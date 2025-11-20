---
name: devops-for-non-dev
description: Git, GitHub, Vercel, and deployment sherpa for non-developers. Use this skill when deploying sites, managing repositories, or learning DevOps basics. Provides step-by-step commands, branching strategies, deployment checklists, and rollback plans.
---

# DevOps-for-Non-Dev Assistant

## Overview

This skill guides you through Git, GitHub, Vercel, and deployment workflows with clear, step-by-step instructions—no DevOps experience required.

**Keywords**: Git, GitHub, Vercel, deployment, version control, continuous deployment, DevOps, hosting, branching

## When to Use This Skill

- Deploy websites to Vercel/Netlify
- Learn Git basics
- Set up repositories
- Manage branches
- Troubleshoot deployment issues
- Set up CI/CD pipelines
- Configure custom domains

## Git Basics - Essential Commands

```
GIT COMMAND CHEAT SHEET
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SETUP (One-time)
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

START A PROJECT
git init                    # Start tracking a folder
git clone [url]             # Download existing repository

DAILY WORKFLOW
git status                  # See what's changed
git add .                   # Stage all changes
git add [file]              # Stage specific file
git commit -m "message"     # Save changes with description
git push                    # Upload to GitHub

BRANCHING
git branch                  # List branches
git branch [name]           # Create new branch
git checkout [name]         # Switch to branch
git checkout -b [name]      # Create and switch to branch
git merge [branch]          # Merge branch into current

UNDO THINGS
git reset [file]            # Unstage file
git checkout -- [file]      # Discard changes
git reset --hard            # DANGER: Discard all changes

CHECK HISTORY
git log                     # See commit history
git diff                    # See uncommitted changes
```

## GitHub Workflow Step-by-Step

```
DEPLOYING YOUR FIRST PROJECT TO GITHUB
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

STEP 1: Create Repository on GitHub
1. Go to github.com
2. Click "New Repository"
3. Name: [your-project-name]
4. Public or Private
5. Don't initialize with README (if you have code locally)
6. Click "Create Repository"

STEP 2: Connect Local Code to GitHub
(Run these commands in your project folder)

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/[username]/[repo].git
git push -u origin main

STEP 3: Verify
- Refresh GitHub page
- You should see your files

DONE! Your code is now on GitHub.
```

## Vercel Deployment Guide

```
DEPLOY TO VERCEL (For Next.js, React, etc.)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

METHOD 1: Connect GitHub (Recommended)

STEP 1: Push code to GitHub (see above)

STEP 2: Connect to Vercel
1. Go to vercel.com
2. Sign up / Log in with GitHub
3. Click "New Project"
4. Select your repository
5. Configure:
   - Framework: [Auto-detected]
   - Root Directory: ./ (usually)
   - Build Command: [Auto-filled]
   - Output Directory: [Auto-filled]
6. Click "Deploy"

STEP 3: Wait for deployment
- Vercel builds your project
- Usually takes 1-2 minutes
- You'll get a URL: [project-name].vercel.app

STEP 4: Set up custom domain (optional)
1. Go to Project Settings → Domains
2. Add your domain
3. Update DNS records (Vercel provides instructions)

DONE! Your site is live and auto-deploys on every Git push.
```

## Branching Strategy (Simple)

```
SIMPLE BRANCHING STRATEGY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

BRANCHES:
- main: Production (always working)
- dev: Development (test here first)
- feature/[name]: New features

WORKFLOW:

1. CREATE FEATURE BRANCH
git checkout -b feature/new-homepage

2. MAKE CHANGES
[Edit files]
git add .
git commit -m "Add new homepage"

3. PUSH FEATURE BRANCH
git push origin feature/new-homepage

4. CREATE PULL REQUEST ON GITHUB
- Go to repository on GitHub
- Click "Pull Requests" → "New Pull Request"
- Base: main ← Compare: feature/new-homepage
- Click "Create Pull Request"
- Review changes
- Click "Merge Pull Request"

5. PULL LATEST TO LOCAL
git checkout main
git pull origin main

6. DELETE FEATURE BRANCH (cleanup)
git branch -d feature/new-homepage
git push origin --delete feature/new-homepage
```

## Common Issues & Solutions

```
TROUBLESHOOTING
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PROBLEM: "Permission denied (publickey)"
SOLUTION:
1. Generate SSH key:
   ssh-keygen -t ed25519 -C "your@email.com"
2. Add to GitHub:
   - Copy: cat ~/.ssh/id_ed25519.pub
   - GitHub Settings → SSH Keys → New SSH key
3. Use SSH URL: git@github.com:[user]/[repo].git

PROBLEM: "Merge conflict"
SOLUTION:
1. Open conflicted files
2. Look for <<<<<<< HEAD markers
3. Choose which code to keep
4. Remove markers
5. git add [file]
6. git commit -m "Resolve conflict"

PROBLEM: "Build failed" on Vercel
SOLUTION:
1. Check Vercel build logs
2. Ensure it builds locally first: npm run build
3. Check Node version matches locally and on Vercel
4. Verify all dependencies in package.json

PROBLEM: Accidentally committed sensitive data
SOLUTION:
1. Remove from tracking:
   git rm --cached [file]
2. Add to .gitignore:
   echo "[file]" >> .gitignore
3. Commit:
   git commit -m "Remove sensitive file"
4. If already pushed: Consider repository history rewrite
```

## Deployment Checklist

```
PRE-DEPLOYMENT CHECKLIST
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CODE READY
□ Code works locally
□ All tests passing (if applicable)
□ No console errors
□ Environment variables documented

GIT READY
□ All changes committed
□ Pushed to GitHub
□ On correct branch
□ .gitignore configured (.env, node_modules, etc.)

VERCEL READY
□ Build command correct
□ Environment variables set in Vercel
□ Custom domain configured (if needed)
□ Analytics set up (optional)

POST-DEPLOYMENT
□ Site loads correctly
□ Test all major features
□ Check mobile responsiveness
□ Monitor for errors
```

## Environment Variables

```
MANAGING SECRETS/ENV VARIABLES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

LOCAL DEVELOPMENT
1. Create .env.local file
2. Add variables:
   NEXT_PUBLIC_API_KEY=abc123
   DATABASE_URL=postgresql://...

3. Add to .gitignore:
   echo ".env.local" >> .gitignore

4. Access in code:
   process.env.NEXT_PUBLIC_API_KEY

VERCEL DEPLOYMENT
1. Go to Project Settings → Environment Variables
2. Add each variable:
   - Name: NEXT_PUBLIC_API_KEY
   - Value: abc123
   - Environment: Production/Preview/Development
3. Redeploy for changes to take effect

IMPORTANT:
- Never commit .env files to Git
- Use NEXT_PUBLIC_ prefix for client-side variables (Next.js)
- Keep sensitive keys server-side only
```

## Rollback Plan

```
HOW TO ROLLBACK A BAD DEPLOYMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ON VERCEL (EASIEST)
1. Go to Deployments tab
2. Find last working deployment
3. Click "..." → "Promote to Production"
DONE! Site rolls back in seconds.

ON GIT (IF NEEDED)
1. Find last working commit:
   git log

2. Revert to that commit:
   git revert [commit-hash]

3. Push:
   git push origin main

Vercel auto-deploys the reverted code.
```

## Getting Started

Tell me:
1. What you want to deploy (Next.js site, React app, etc.)
2. Current stage (local code / on GitHub / deployed)
3. Any issues you're facing

I'll provide step-by-step commands.
