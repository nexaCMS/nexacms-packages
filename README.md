# NexaCMS Official Packages

The official plugin & theme catalog for [NexaCMS](https://github.com/nexaCMS/NexaCMS).

## For users

You don't need to do anything with this repo directly. In NexaCMS go to
**Admin → Plugins → Repositories** — this catalog is pre-registered on new
installs as **"NexaCMS Official Packages"**, and you can browse and install
any plugin or theme with one click. Every package is verified against the
SHA-256 hash in `nexa-repo.json` before it is installed.

To add it manually (older installs): Repositories → Add → type **GitHub**,
repository `nexaCMS/nexacms-packages`, branch `main`.

## For maintainers

- `nexa-repo.json` is the machine-readable index (type, slug, version,
  description, `download_url`, `sha256` per package).
- `packages/<slug>.zip` holds one installable zip per plugin/theme
  (top-level folder inside the zip, the standard NexaCMS package format),
  served to installs via raw.githubusercontent.com URLs.
- To publish an update: replace the zip, refresh its `sha256` and
  `version` in `nexa-repo.json`, commit, push. Installed sites see the new
  version flagged in Repositories on their next visit.

Catalog built from the NexaCMS 1.33.1 release. GPL-3.0.
