# Prompts

This repository contains the system prompts used by the Ressl AI agents. These prompts are fetched dynamically from GitHub and cached in the application.

## Prompt Files

- `analysis.prompt` - Used by the analysis agent for deep Salesforce metadata analysis
- `execution.prompt` - Used by the execution agent for implementing plans step by step
- `planning.prompt` - Used by the planning agent for creating execution plans
- `process_flow.prompt` - Used by the process flow agent for detailed business process analysis

## Usage

The prompts are automatically fetched from this repository when the application starts and are refreshed via GitHub webhooks when changes are pushed to the main branch.

### Fetching Prompts

The application fetches prompts using the following URL pattern:
```
https://raw.githubusercontent.com/ResslAI-Salesforce/prompts/main/{prompt_name}.prompt
```

### Webhook Integration

When changes are pushed to this repository, a webhook triggers the application to refresh all prompts in the background.

## Development

To modify prompts:

1. Edit the appropriate `.prompt` file
2. Commit and push to the main branch
3. The webhook will automatically refresh the prompts in the application


