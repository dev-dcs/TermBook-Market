# TermBook Market

The index TermBook's market reads (Market > Plugins > Online index), plus
the plugins it points to.

@Dev_DcS

## Layout

```
index.tsv          what the market lists
plugins/<name>/    one folder per plugin (see TermBook's docs/plugin-format.md)
```

## index.tsv

One entry per line, fields separated by tabs; lines starting with `#` are
comments.

```
kind	id	name	description	source
```

- `plugin`: `source` is an https git link. `repo#plugins/name` installs the
  plugin from that folder of the repository.
- `package`: `source` is one or more package names, installed with
  `tb-install` (pacman or apt, whichever the userland has).

## Publishing

The repository must be public: TermBook reads
`https://raw.githubusercontent.com/dev-dcs/TermBook-Market/main/index.tsv`
without signing in. Keep the branch named `main`, or change the index link
in the app.
