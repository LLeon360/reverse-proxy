# Reverse Proxy in Deno

## Usage

Define hosts directly to the `getBackend()` function in `main.ts` for now.  

Configure allowed accounts and the hash of the password in `config.json` and whether auth is required at all.

Run with 
```
deno task dev
```

Then this will listen to incoming requests on port `8080` unless otherwise changed in `main.ts` by editing  `const listener = Deno.listen({ port: <desired port> });`. The request will be proxied to the corresponding backend.

Requests and errors will be logged to the log files defined in the config.
