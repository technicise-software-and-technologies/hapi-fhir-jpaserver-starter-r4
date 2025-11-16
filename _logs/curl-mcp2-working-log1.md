curl -X POST http://localhost:8080/mcp/messages \
  -H "Content-Type: application/json" \
  -H "Accept: application/json, text/event-stream" \
  -d '{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "initialize",
    "params": {
      "protocolVersion": "2024-11-05",
      "capabilities": {},
      "clientInfo": {
        "name": "test-client",
        "version": "1.0.0"
      }
    }
  }'
{"jsonrpc":"2.0","id":1,"result":{"protocolVersion":"2024-11-05","capabilities":{"completions":{},"logging":{},"prompts":{"listChanged":true},"resources":{"subscribe":false,"listChanged":true},"tools":{"listChanged":true}},"serverInfo":{"name":"FHIR MCP Server","version":"1.0.0"},"instructions":"This server provides access to a FHIR RESTful API. You can use it to query FHIR resources, perform operations, and retrieve data in a structured format."}}chandra@chandra-latitude-ubuntu22:/media/chandra/b664505e-129c-4c0d-a87b-9efb6469eca2/home/chandra/code/hapi-fhir-jpaserver-starter$ 

