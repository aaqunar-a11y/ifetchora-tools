# ifetchora-tools

Small, single-file browser tools. One tool, one problem, no build step, no
dependencies, no network access at runtime.

Each tool lives in `tools/<name>/` and is downloadable from its own release.
Everything is MIT licensed.

| Tool | What it solves | Size | Offline | Source | Use it |
|---|---|---|---|---|---|
| **File Hash Checker** | Check a downloaded file against the checksum its publisher published, and find out *why* the values differ when they do | 31624 bytes | yes | [source](https://github.com/aaqunar-a11y/ifetchora-tools/tree/file-hash-checker-v1.0.0/tools/file-hash-checker/) | [https://ifetchora.com/tools/file-hash-checker/](https://ifetchora.com/tools/file-hash-checker/) |

## Why these tools look the way they do

* **One problem per tool.** No dashboards, no toolboxes, no settings pages.
* **A single file.** HTML, CSS and JavaScript in one file. Open it from disk
  and it works with the network disconnected.
* **Nothing leaves your machine.** No upload, no analytics, no CDN, no
  third-party script. There is no server component to leak anything.
* **Published checksums.** Every release ships the exact bytes of the tool plus
  a `SHA256SUMS` file, so you can verify the copy you downloaded.

## Verify a download

```
# after downloading file-hash-checker.html from its release:
sha256sum file-hash-checker.html
# compare with the value in the release's SHA256SUMS
```

Or simply open the tool and drop the tool into itself.

## License

MIT. See [LICENSE](https://github.com/aaqunar-a11y/ifetchora-tools/blob/main/LICENSE).
