# procursus-action
Bootstraps the Procursus toolchain onto a macOS runner. 

## fuck is Procursus?
[Procursus](https://github.com/ProcursusTeam/Procursus) is a build-system that provides a large set of consistently up-to-date *nix tools cross compiled to work on Darwin based platforms.

## Usage
Only macOS 11 and newer runners (`macos-latest`), since Procursus itself only compiles for Darwin-based platforms.

```yaml
- uses: beerpiss/procursus-action@v1.2
  with:
    packages:  # A space-delimited list of what to install after bootstrapping (etc. 'clang cmake')
    cache:  # Whether to cache the bootstrap for faster runs (default true)

```

## Issues
Feel free to submit any issues or pull requests.

### Known issues
- /opt/procursus/bin/dpkg exits with error code 100. Restart workflow, I don't know why this happens /shrug

## License

This project is released under the [0BSD License](LICENSE)
