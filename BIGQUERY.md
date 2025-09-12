# BigQuery Extension

This document provides instructions for the Gemini agent to assist users with the BigQuery extension.

## BigQuery MCP Server (Data Plane: Connecting and Querying)

This section covers connecting to a BigQuery instance.

1. **Verify Environment Variables**: Before attempting to connect, confirm with the user that the following environment variables are set in the extension configuration or their shell environment.

    * `BIGQUERY_PROJECT`: The GCP project ID.

2. **Handle Missing Variables**: If a command fails with an error message containing a placeholder like `${BIGQUERY_PROJECT}`, it signifies a missing environment variable. Inform the user which variable is missing and instruct them to set it.

3. **Handle Permission Errors**: If you encounter permission errors, ensure the user has the correct BigQuery permissions (e.g., `bigquery.jobs.create`, `bigquery.datasets.getData`, `bigquery.tables.list`).
