### OpenAPI Generator
## ASP Net Core Bearer Auth Roles Test

Demo repo to test behaviour of bearer auth scopes/roles during ASP Net Core server code generation.

### Related Issues:
https://github.com/OpenAPITools/openapi-generator/issues/1983

### Repro Steps
```
npm install
npm run build
```

### Current Output
`PetsApi.cs` routes are annotated with `[Authorize]` with no roles defined

### Expected Output
`PetsApi.cs` routes to be annotated with `[Authorize(Roles="User","Admin")]`
