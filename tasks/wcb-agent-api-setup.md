# WCB Agent API Setup (Safe)

## Docs
- https://web3career.build/llms.txt
- Base URL: `https://web3career.build`
- Catalog: `GET /api/agent/catalog`
- Call endpoint: `POST /api/agent/call`

## Secret Management
Never commit secrets to git.
Use local env var only:

```bash
export WCB_AGENT_SECRET_API_KEY="<your_secret_key>"
```

## Verify Access
```bash
curl -s https://web3career.build/api/agent/catalog \
  -H "Authorization: Bearer $WCB_AGENT_SECRET_API_KEY"
```

## Procedure Call Template
```bash
curl -s https://web3career.build/api/agent/call \
  -H "Authorization: Bearer $WCB_AGENT_SECRET_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"procedure":"users.getProfile","input":{}}'
```

## Learner-side useful procedures
- `users.getProfile`
- `users.getMyPermissions`
- `tasks.listForLearner`
- `tasks.myTaskHistory`
- `tasks.submitEvidence`
- `events.listForLearner`
