# Plagium API Documentation

Interactive API documentation for the [Plagium](https://www.plagium.com) REST API v3 — plagiarism detection service by [Septet Systems](https://www.septetsystems.com).

## Documentation

**https://septetsystems.github.io/plagium-api-docs/**

Powered by [Swagger UI](https://swagger.io/tools/swagger-ui/) and the [OpenAPI 3.0.3](https://spec.openapis.org/oas/v3.0.3) specification.

## Endpoints

| Group | Endpoint | Description |
|---|---|---|
| **Documents** | `POST /300/document/create` | Create a plagiarism check from text or URL |
| | `POST /300/document/upload` | Create a check by uploading a file |
| | `POST /300/document/get` | Retrieve a document by ID |
| | `POST /300/document/list` | List documents with filters |
| | `POST /300/document/results` | Get plagiarism detection results |
| | `POST /300/document/embedded-report-url` | Get embeddable report URLs |
| **Account** | `POST /300/account/remaining_credits` | Get remaining credits |
| **Sub-Accounts** | `POST /300/sub_account/create` | Create a sub-account |
| | `POST /300/sub_account/list` | List sub-accounts |
| | `POST /300/sub_account/add_credits` | Add credits to a sub-account |
| | `POST /300/sub_account/remaining_credits` | Get sub-account credits |
| **Search** | `POST /300/search/quick` | Quick plagiarism web search |

## Authentication

All endpoints require a `key` parameter in the request body. An optional `password` is used when the API password is enabled on the account.

```json
{
  "key": "YOUR_API_KEY",
  "data": { ... }
}
```

## License

Copyright Septet Systems. All rights reserved.
