# Coolify Deploy Action

Triggers a Coolify deployment and polls for completion.

## Usage

```yaml
- name: Deploy to Coolify
  uses: mikipavlov/coolify-deploy-action@v1
  with:
    domain: ${{ steps.config.outputs.domain }}
    uuid: ${{ steps.config.outputs.uuid }}
    token: ${{ secrets.COOLIFY_API_KEY }}
```

## Inputs

| Input  | Description | Required |
|--------|-------------|----------|
| domain | Coolify instance domain (e.g., https://coolify.example.com) | Yes |
| uuid   | Application UUID to deploy | Yes |
| token  | Coolify API token (needs 'read' permission for polling) | Yes |

## Requirements

- `jq` must be available in the runner
- API token must have 'read' permission for deployment status polling
