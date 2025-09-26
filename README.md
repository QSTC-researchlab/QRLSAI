# QRLSAI

## Environment Setup

1. Copy the example environment file to create your local secrets file:
   ```bash
   cp .env.example .env
   ```
2. Open `.env` and replace every placeholder with the real values for your deployment.
3. Restart any running services so they pick up the new configuration.

### Environment Variable Reference

| Variable | Purpose | Example |
| --- | --- | --- |
| `JWT_ACCESS_SECRET` | Secret key used to sign short-lived JSON Web Tokens issued to clients. | `super-secret-access-key` |
| `JWT_REFRESH_SECRET` | Separate secret used to sign refresh tokens for issuing new access tokens. | `another-refresh-secret` |
| `REDIS_URL` | Connection string for the Redis instance that backs caching, queues, and rate limiting. | `redis://localhost:6379/0` |
| `OPENAI_API_KEY` | API key used to authenticate with OpenAI services. | `sk-your-openai-key` |
| `ANTHROPIC_API_KEY` | API key used to authenticate with Anthropic services. | `anthropic-your-key` |
| `GOOGLE_API_KEY` | API key for Google services (e.g., Vertex AI or Google Cloud). | `AIza-your-google-key` |
| `PRIVACY_LOCK_DEFAULT` | Sets the default privacy lock state applied to newly created resources (`true`/`false`). | `false` |

Refer to `.env.example` for an annotated template of all required variables.
