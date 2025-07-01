# mcp

1. Change default application login: if you are running on a Google Compute Engine virtual machine, the service credentials associated with this virtual machine will automatically be used by Application Default Credentials. To change to a user account's credentials instead, run this command ```gcloud auth application-default login```

1. Configure your mcp servers
   1. Local servers
   In ~/.gemini/settings.json, add the following lines
   ```json
   "mcpServers": {
    "cloud-run": {
     "command": "npx",
     "args": ["-y", "https://github.com/GoogleCloudPlatform/cloud-run-mcp"]
    }
   }
   ```
   
   1. Restart Gemini CLI if it is running. Otherwise, Gemini CLI won't start the local server and won't recognize there is an MCP to use.