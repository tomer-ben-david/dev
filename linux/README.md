## TCPDUMP Textual

```bash
tcpdump -A -iany port 8080 -w scoring-conf-req.tcpdump
```

## Which process listens on port

```bash
lsof -n -i:4888 | grep LISTEN
```

`-n` causes it to run much faster (do not resolve host names)
