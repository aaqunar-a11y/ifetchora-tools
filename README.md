# ifetchora-tools

Small, single-file browser tools. One tool, one problem, no build step, no
dependencies, no network access at runtime.

Each tool lives in `tools/<name>/` and is downloadable from its own release.
Everything is MIT licensed.

| Tool | What it solves | Size | Offline | Source | Use it |
|---|---|---|---|---|---|
| **File Hash Checker** | Check a downloaded file against the checksum its publisher published, and find out *why* the values differ when they do | 31624 bytes | yes | [source](https://github.com/aaqunar-a11y/ifetchora-tools/tree/file-hash-checker-v1.0.0/tools/file-hash-checker/) | [https://ifetchora.com/tools/file-hash-checker/](https://ifetchora.com/tools/file-hash-checker/) |
| **Text Diff Checker** | Compare two blocks of text and see exactly which lines and words differ, including the differences that are invisible on screen &mdash; trailing whitespace, tab/space swaps, confusable characters, and CRLF vs LF | 31039 bytes | yes | [source](https://github.com/aaqunar-a11y/ifetchora-tools/tree/text-diff-checker-v1.0.0/tools/text-diff-checker/) | [https://ifetchora.com/tools/text-diff-checker/](https://ifetchora.com/tools/text-diff-checker/) |

## Why these tools look the way they do

* **One problem per tool.** No dashboards, no toolboxes, no settings pages.
* **A single file.** HTML, CSS and JavaScript in one file. Open it from disk
  and it works with the network disconnected.
* **Nothing leaves your machine.** No upload, no analytics, no CDN, no
  third-party script. There is no server component to leak anything. Files you
  load into a tool are read by your own browser and go nowhere.
* **Published checksums.** Every release ships the exact bytes of the tool plus
  a `SHA256SUMS` file, so you can verify the copy you downloaded.

## Verify a download

```
# after downloading a tool from its release (text-diff-checker.html here):
sha256sum text-diff-checker.html
# compare with the value in the release's SHA256SUMS
```

The hash checker can also verify *itself*: open it and drop the tool into it.

## License

MIT. See [LICENSE](https://github.com/aaqunar-a11y/ifetchora-tools/blob/main/LICENSE).
