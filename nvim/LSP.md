For the typescript LSP to work in JS progect a `jsconfig.json` file is required:

```json
{
	"$schema": "https://raw.githubusercontent.com/SchemaStore/schemastore/master/src/schemas/json/jsconfig.json",
	"compilerOptions": {
		"checkJs": true
	}
}
```
