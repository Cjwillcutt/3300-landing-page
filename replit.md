# 3300 Landing Page

## Project Overview
A simple static HTML landing page ("Hello World").

## Structure
- `index.html` — Main HTML file served as the landing page
- `Test` — Another static HTML file

## Running the Project
The app is served using Python's built-in HTTP server on port 5000:
```
python3 -m http.server 5000 --bind 0.0.0.0
```

## Deployment
Configured as a static site deployment with `publicDir: "."`.
