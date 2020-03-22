---
# This file is automatically generated from the API using `sentry/api-docs/generator.py.`
# Do not manually edit this file.
{
  "api_path": "/api/0/projects/{organization_slug}/{project_slug}/stats/", 
  "authentication": "required", 
  "description": "Return a set of points representing a normalized timestamp and the\nnumber of events seen in the period.\n\nQuery ranges are limited to Sentry's configured time-series\nresolutions.", 
  "example_request": "GET /api/0/projects/the-interstellar-jurisdiction/pump-station/stats/ HTTP/1.1\nHost: sentry.io\nAuthorization: Bearer <token>", 
  "example_response": "HTTP/1.1 200 OK\nContent-Length: 476\nX-XSS-Protection: 1; mode=block\nX-Content-Type-Options: nosniff\nContent-Language: en\nAccess-Control-Expose-Headers: X-Sentry-Error, Retry-After\nVary: Accept-Language, Cookie\nAccess-Control-Allow-Methods: GET, HEAD, OPTIONS\nAllow: GET, HEAD, OPTIONS\nAccess-Control-Allow-Origin: *\nAccess-Control-Allow-Headers: X-Sentry-Auth, X-Requested-With, Origin, Accept, Content-Type, Authentication, Authorization\nContent-Type: application/json\nX-Frame-Options: deny\n\n[\n  [\n    1584824400.0, \n    927\n  ], \n  [\n    1584828000.0, \n    877\n  ], \n  [\n    1584831600.0, \n    1071\n  ], \n  [\n    1584835200.0, \n    1387\n  ], \n  [\n    1584838800.0, \n    1978\n  ], \n  [\n    1584842400.0, \n    1391\n  ], \n  [\n    1584846000.0, \n    763\n  ], \n  [\n    1584849600.0, \n    1058\n  ], \n  [\n    1584853200.0, \n    1059\n  ], \n  [\n    1584856800.0, \n    1619\n  ], \n  [\n    1584860400.0, \n    1019\n  ], \n  [\n    1584864000.0, \n    1127\n  ], \n  [\n    1584867600.0, \n    1257\n  ], \n  [\n    1584871200.0, \n    1950\n  ], \n  [\n    1584874800.0, \n    1213\n  ], \n  [\n    1584878400.0, \n    1030\n  ], \n  [\n    1584882000.0, \n    1159\n  ], \n  [\n    1584885600.0, \n    1380\n  ], \n  [\n    1584889200.0, \n    780\n  ], \n  [\n    1584892800.0, \n    1089\n  ], \n  [\n    1584896400.0, \n    902\n  ], \n  [\n    1584900000.0, \n    1786\n  ], \n  [\n    1584903600.0, \n    1906\n  ], \n  [\n    1584907200.0, \n    1899\n  ]\n]", 
  "method": "GET", 
  "parameters": null, 
  "path_parameters": [
    {
      "description": "the slug of the organization.", 
      "name": "organization_slug", 
      "type": "string"
    }, 
    {
      "description": "the slug of the project.", 
      "name": "project_slug", 
      "type": "string"
    }
  ], 
  "query_parameters": [
    {
      "description": "the name of the stat to query (`\"received\"`, `\"rejected\"`, `\"blacklisted\"`, `generated`)", 
      "name": "stat", 
      "type": "string"
    }, 
    {
      "description": "a timestamp to set the start of the query in seconds since UNIX epoch.", 
      "name": "since", 
      "type": "timestamp"
    }, 
    {
      "description": "a timestamp to set the end of the query in seconds since UNIX epoch.", 
      "name": "until", 
      "type": "timestamp"
    }, 
    {
      "description": "an explicit resolution to search for (one of `10s`, `1h`, and `1d`)", 
      "name": "resolution", 
      "type": "string"
    }
  ], 
  "sidebar_order": 18, 
  "title": "Retrieve Event Counts for a Project", 
  "warning": "This endpoint may change in the future without notice."
}
---