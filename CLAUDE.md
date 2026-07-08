# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for the **RAISE (Research on Advanced Information Systems Engineering) Group** at Politecnico di Milano (DEIB). Hosted on GitHub Pages at https://raisegroup-polimi.github.io.

## Commands

```bash
# Serve locally with live reload
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

## Architecture

**Jekyll static site** using the [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll) remote theme (`daattali/beautiful-jekyll`). No custom `_layouts` or `_includes` — all templating comes from the upstream theme.

Content files:
- `index.markdown` — Homepage (research topics, team)
- `about.markdown` — About page
- `spatial.makdown` — Spatial systems research page (note: typo in filename, `.makdown`)
- `static/` — All static assets: group logos, academic networking icons (LinkedIn, Scholar, DBLP), and member profile photos in `static/profile/`

Each page uses Jekyll front matter to declare its layout and permalink:
```yaml
---
layout: page
title: "Page Title"
permalink: /path/
---
```

Images in markdown must use paths relative to site root (e.g., `/static/image.png`), not relative file paths.
