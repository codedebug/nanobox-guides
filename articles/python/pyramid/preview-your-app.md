# Preview your App

_**PLACEHOLDER:** This whole guide is essentially placeholder content and needs to be replaced with Pyramid-specific content._

Nanobox allows you to test your app in a production environment, locally, before you actually launch it into production with `dry-run`.

## Add a preview DNS
Add a convenient way to access your app from the browser:

```bash
nanobox dns add dry-run pyramid.test
```

**HEADS UP**: You'll need to add `pyramid.st` to the list of `ALLOWED_HOSTS` in `app/settings.py`

## dry-run the app

```bash
nanobox deploy dry-run
```

Visit your app at <a href="http://pyramid.st" target="\_blank">http://pyramid.st</a>

With `dry-run` your app will continue to run until stopped (`ctrl + c`). This allows you to to preview it, watch logs, seed data, and troubleshoot.

**HEADS UP**: You can add environment variables to dry-run the same way you do [locally](/python/pyramid/local-evars) with `nanobox evar add dry-run KEY=VALUE`.
