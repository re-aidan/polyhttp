# pollyhttp

A HTTP client built from raw TCP sockets, in as many languages as possible. Without any HTTP libraries.

## The rules

I may use:

- the language's raw socket API (`socket`, `TcpStream`, `net.Dial)
- the language's standard TLS library, for HTTPS only

Implementations may **not** use any HTTP client library (`requests`, `axios`, `reqwest`, `=WEBSERVICE()`, `…`).

## What's done

| Language | Status |
|---|---|
|Python|Not started|

## Running one

Every implementation exposes the same CLI. See [`spec/cli-contract.md`](spec/cli-contract.md).

```
cd implementations/python
./run.sh GET http://127.0.0.1:8080/fixtures/plain
```

## License

MIT