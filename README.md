# DEADLINE & TARTIP — v1 starter

A responsive Twitch-inspired streaming platform frontend using the official D&T palette:
- Navy: `#080B12`
- Electric blue: `#0757D9`
- Ice blue: `#00A9FF`
- Snow white: `#F4F8FF`
- LIVE red: `#FF4358`

## Run locally
Open `index.html` in a browser. For best results, use a local static server or VS Code Live Server.

## Enable real Supabase accounts
1. Open `app.js`.
2. Replace `YOUR_SUPABASE_PROJECT_URL` with the Project URL from Supabase Project Settings → API.
3. Replace `YOUR_SUPABASE_ANON_PUBLIC_KEY` with the anon/public key.
4. Never use the `service_role` key in frontend code.
5. Ensure the `profiles` table and auth trigger have been created in Supabase.

The signup form sends `display_name` metadata to Supabase Auth. The database trigger created earlier can use that metadata to create a profile.

## Important next steps
- Configure Supabase Row Level Security policies for each feature.
- Create a secure server-side admin workflow. Do not let users grant themselves `owner`, `admin`, `verified`, or `premium` roles from the browser.
- GitHub Pages can host this frontend. Real live video requires a separate WebRTC signaling/media infrastructure; this starter only contains the UI preview.
