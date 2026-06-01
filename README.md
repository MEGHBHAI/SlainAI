# SlainAI Backend for Netlify

This backend is set up to run as a Netlify Python function.

## Deploying to Netlify

1. Create a new Netlify site and point it at the `backend` folder in this repo.
2. Set the build settings:
   - Build command: none required
   - Publish directory: `.`
3. Add the environment variable `GROQ_API_KEY` in Netlify site settings.

## Backend endpoint

The frontend expects the backend at `/chat` on the deployed Netlify site.
The `netlify.toml` file rewrites `/chat` to the function at `/.netlify/functions/chat`.

## Local development

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Run locally:

```bash
python app.py
```

Then POST to `http://localhost:5000/chat`.
