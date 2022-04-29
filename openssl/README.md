# openssl

Put it in your pipe:

```bash
docker build -t openssldocker .
```

and smoke it:

```bash
docker run -it --rm -v $(pwd):/apps -w /apps openssldocker <command>
```
