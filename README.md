# LiveBook

This is just a simple docker-compose set up for Elixir LiveBook.

Check out the following links for more information about LiveBook:

- https://livebook.dev/
- https://github.com/livebook-dev/livebook

## Setup

You can start LiveBook with `docker compose up` which will start the app locally
at <http://localhost:8080>. The default set up here is to generate a random
password (which will be output by in the livebook application logs).

```
> docker compose up
Attaching to livebook-livebook-1
livebook-livebook-1  | [Livebook] Application running at http://localhost:8080?token=b5ofktkc2nvd7r6n4jtjus77r6flgw2f
```

If you want to specify your own password, you can set the `LIVEBOOK_PASSWORD`
environment variable. There's a disabled setup for the `.env` in the
`docker-compose.yml` and a `.env.example` you can use as a template.

Compose will mount the folder `./notebooks` to `/data` in the container so that
you can preserve your notebooks between sessions.
