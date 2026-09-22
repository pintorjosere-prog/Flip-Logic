# Flip Logic Auth Setup

## Live target
https://fliplogic.pages.dev
(Fallback while Pages is pending: https://pintorjosere-prog.github.io/Flip-Logic/)

## Supabase project
Name: Real Estate AI
Ref: upuhrwpdlfavnpfzdjrc
URL: https://upuhrwpdlfavnpfzdjrc.supabase.co
(Anon key is wired in index.html as FLIPLOGIC_SUPABASE_ANON_KEY.)

## App auth behavior
- UI: Sign in with Google (any Google account — Workspace or Gmail)
- Method: supabase.auth.signInWithOAuth({ provider: "google" })
- No client-side Gmail-only restriction

## Configure Google provider
1. Authentication → URL Configuration
   - Site URL: https://fliplogic.pages.dev
   - Redirect URLs: https://fliplogic.pages.dev/** and https://pintorjosere-prog.github.io/Flip-Logic/**
2. Authentication → Providers → Google → Enable
3. Google Cloud Console → APIs & Services → Credentials → OAuth 2.0 Client ID (Web)
   - Authorized JavaScript origins: https://fliplogic.pages.dev , https://pintorjosere-prog.github.io
   - Authorized redirect URIs: https://upuhrwpdlfavnpfzdjrc.supabase.co/auth/v1/callback
4. Paste Client ID + Client Secret into Supabase Google provider → Save
5. If consent screen is in Testing, add test users (or publish app)

## Verify
Open https://fliplogic.pages.dev → Sign in with Google → land back in the app with session.
