# argvus-devtools

An Arch Linux metapackage for development tools and programming utilities. It
installs no editor configuration, source files, or application payload; pacman
installs the declared dependencies.

[![CI](https://github.com/argvus/argvus-devtools/actions/workflows/ci.yml/badge.svg)](https://github.com/argvus/argvus-devtools/actions/workflows/ci.yml)
[![Release](https://github.com/argvus/argvus-devtools/actions/workflows/release.yml/badge.svg)](https://github.com/argvus/argvus-devtools/actions/workflows/release.yml)
[![License](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](LICENSE)

## Dependencies

Required: `code`, `neovim`, `git`, `less`, `tree`, `starship`, `zsh`,
`ripgrep`, `fd`, `fzf`, `bat`, `eza`, `btop`, `jq`, `curl`, `wget`, `openssh`,
`zip`, `gcc`, `clang`, `gdb`, `lldb`, `cmake`, `ninja`, `meson`, `pkgconf`,
`strace`, `valgrind`, `python-pip`, `nodejs`, `npm`, `go`, `shellcheck`, and
`openai-codex`.

Optional: `docker` and `podman`, which overlap as container engines. Rust
toolchains and language servers are not included in this profile.

## Build and validate

On Arch Linux or a compatible distribution with the skeleton's build tools:

```sh
make validate
make build
```

`make build` writes the local source archive and build artifacts under
`build/artifacts/`, and the package under `build/dist/`. `make install` installs
the package and therefore requires administrator privileges; it is not needed
to build or inspect it.

See [DEVELOPMENT.md](DEVELOPMENT.md) and
[packaging/archlinux/README.md](packaging/archlinux/README.md) for packaging
details.

## License

SPDX: `GPL-3.0-only`. See [LICENSE](LICENSE).
