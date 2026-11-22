# scoop-bucket

[![Tests](https://github.com/goetterbote2342/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/goetterbote2342/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/goetterbote2342/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/goetterbote2342/scoop-bucket/actions/workflows/excavator.yml)

Personal [Scoop](https://scoop.sh) bucket for apps that are not in `main` or `extras`.

## Install

```pwsh
scoop bucket add goetterbote https://github.com/goetterbote2342/scoop-bucket
scoop install goetterbote/<app>
```

## Apps

| App | Description |
| --- | --- |
| `ompanion` | GUI client for [omp](https://omp.sh) (oh-my-pi), on this computer and remote machines over SSH and Tailscale. Windows 10 1809+, needs the WebView2 Runtime (included in Windows 11). |

Manifests are kept at the latest upstream release by the Excavator workflow (`checkver` + `autoupdate`).

## Layout

`bucket/` holds one manifest per app, `bin/` the Scoop helper scripts (`checkver.ps1`, `test.ps1`, …). Run `.\bin\test.ps1` to lint and validate before pushing; CI does the same on Windows.
