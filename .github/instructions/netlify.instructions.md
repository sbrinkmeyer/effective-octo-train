# Netlify Deployment Instructions

Apply these rules whenever working on deployment or hosting behavior.

## Scope
- `netlify.toml`
- Build commands and publish directory
- Redirect/headers files and behavior
- Environment variable strategy

## Rules
- Prefer repository-based configuration over manual dashboard settings.
- Never commit secrets; reference environment variables instead.
- Keep production and deploy-preview behavior consistent unless intentionally different.
- Document any required Netlify UI settings that cannot be versioned.

## Hugo defaults
- Typical build command: `hugo --gc --minify`
- Typical publish directory: `public`

## Quality checks
- Validate that branch deploy and production deploy settings match expectations.
- Confirm redirects and headers are unambiguous and non-conflicting.
