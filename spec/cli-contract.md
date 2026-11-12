## Invocation

```
run.sh METHOD URL [flags]
```

`METHOD` is `GET` 

| Flag | Meaning |
|---|---|
| `-H "Name: Value"` | Add a request header. |
| `--timeout MS` | Connect + read timeout. Default `5000`. |
| `--insecure` | Skip TLS certificate verification. |

## stdout

```
STATUS: <code>
<name>: <value>
<name>: <value>

<decoded body>
```

## Exit codes

| Code | Meaning |
|---|---|
| `0` | Exchange completed. **Any status code**. |
| `1` | Client failure: DNS, connection refused, timeout, TLS error, malformed response. |
| `2` | Usage error: bad flags, unparseable URL. |

## Example

```
$ ./run.sh GET http://127.0.0.1:8080/fixtures/plain
STATUS: 200
content-length: 12
content-type: text/plain

hello world
```

The body is the 12 bytes `hello world\n`.