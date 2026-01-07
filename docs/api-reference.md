# API Reference

## Authentication
Velocity uses API keys to allow access to the API. You can register a new API key at our [developer portal](https://platform.veloo.io).

Velocity expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer YOUR_API_KEY`

## Endpoints

### POST /v1/render
Creates a new render job.

**Parameters:**
- `template_id` (string): The ID of the template to render.
- `data` (object): Key-value pairs for dynamic replacement.

**Response:**
```json
{
  "job_id": "job_12345",
  "status": "queued"
}
```

### GET /v1/jobs/{job_id}
Check the status of a render job.
