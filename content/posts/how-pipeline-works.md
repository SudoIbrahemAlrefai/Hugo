---
title: "How Our CI/CD Pipeline Works"
date: 2026-03-29T11:00:00
draft: false
tags: ["AWS", "CI/CD", "Hugo"]
---

Our deployment pipeline has three stages:

**Source** — AWS CodePipeline watches our GitHub repo for pushes to the main branch.

**Build** — AWS CodeBuild downloads Hugo, runs the build, and outputs the static site files.

**Deploy** — The built files are extracted and uploaded to our S3 bucket, which serves them as a static website.

The entire process takes about two minutes from push to live site.
