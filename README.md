# zenginx

`zenginx` is a zero-configuration `nginx` wrapper to run command-line servers.

By default, it will work as a static file server on port `8080`, and serve the current working directory:

```bash
$ zenginx
Listening on localhost:8080
Starting file server on /home/me/
```

You can specify the port to serve on and the path to mount using `--port` and `--dir`:

```bash
$ zenginx --port 3000 --dir www
Listening on localhost:3000
Starting file server on /home/me/www
```

You can also use `zenginx` to set up a proxy:

```
$ zenginx --port 3000 --proxy http://google.com
Listening on localhost:3000
Starting HTTP proxy to http://google.com
```

See `zenginx --help` for more info.


## Installation

Make sure you have `nginx` in your path, and just copy the `bin/zenginx` file from this repository.