# luaupm index

The default package index for [lpm](https://github.com/luaupm/cli), the Luau
package manager.

- `config.toml` — index configuration read by lpm.
- `<scope>/<name>` — one TOML file per package, keyed by `"<version> <target>"`,
  each entry carrying a direct `download` URL, target, and dependencies.
- `<scope>/owners.toml` — GitHub logins allowed to publish in a scope; the
  first publish to a scope claims it.

`lpm publish` uploads your package as a GitHub release asset and opens a PR
here adding the index entry. Packages go live when the PR merges.
