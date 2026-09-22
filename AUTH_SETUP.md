# Flip Logic Auth Setup

## Live target
https://fliplogic.pages.dev

## Supabase (free)
1. Create/use free project
2. Authentication → Providers → Google → enable
3. Site URL: https://fliplogic.pages.dev
4. Redirect URLs: https://fliplogic.pages.dev/**
5. Google Cloud OAuth client:
   - Authorized JS origins: https://fliplogic.pages.dev
   - Authorized redirect URIs: https://<PROJECT_REF>.supabase.co/auth/v1/callback
6. Paste Client ID + Secret into Supabase Google provider
7. Put project URL + anon key into index.html (FLIPLOGIC_SUPABASE_URL / FLIPLOGIC_SUPABASE_ANON_KEY)

## Gmail-only
Client gate: email must end with @gmail.com or @googlemail.com; otherwise Access denied + sign out.
