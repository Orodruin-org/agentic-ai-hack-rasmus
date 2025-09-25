# Azure Function Orchestrator Setup

## Environment Configuration

This Azure Function requires several environment variables to be configured in `local.settings.json`. 

### Setup Instructions

1. Copy the template file:
   ```bash
   cp local.settings.json.template local.settings.json
   ```

2. Replace the placeholder values in `local.settings.json` with your actual Azure resource endpoints and keys:
   - `AI_FOUNDRY_PROJECT_ENDPOINT`: Your AI Foundry project endpoint
   - `MODEL_DEPLOYMENT_NAME`: Your deployed model name (e.g., "gpt-4o-mini")
   - `COSMOS_ENDPOINT`: Your Cosmos DB endpoint
   - `COSMOS_KEY`: Your Cosmos DB primary key
   - `AZURE_OPENAI_ENDPOINT`: Your Azure OpenAI service endpoint
   - `AZURE_OPENAI_KEY`: Your Azure OpenAI API key
   - `SEARCH_SERVICE_ENDPOINT`: Your Azure Cognitive Search service endpoint
   - `SEARCH_ADMIN_KEY`: Your Azure Cognitive Search admin key

### Security Note

⚠️ **Never commit `local.settings.json` to version control** - it contains sensitive keys and secrets. The file is already listed in `.gitignore` to prevent accidental commits.

### Running the Function

```bash
func host start
```