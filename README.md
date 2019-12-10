Possible TS Build Bug
---

Using `tsc --build --listEmittedFiles` will not output any file, but will list as if files were emitted.

### Steps to replicate:

1. Clone this repo
2. `yarn`
3. Build once: `yarn tsc --build`
4. Remove output `rm -rf lib`
5. Rebuild: `yarn tsc --build --listEmittedFiles`
6. Observe; no files outputted, although TSC lists "emitted" files.
