# procursus-action
Bootstraps the Procursus toolchain onto a macOS runner. 

## fuck is Procursus?
[Procursus](https://github.com/ProcursusTeam/Procursus) is a build-system that provides a large set of consistently up-to-date *nix tools cross compiled to work on Darwin based platforms.

## Usage
Only macOS 11 and newer runners (`macos-latest`), since Procursus itself only compiles for Darwin-based platforms.

```yaml
- uses: beerpiss/procursus-action@v1.3
  with:
    packages:  # A space-delimited list of what to install after bootstrapping (etc. 'clang cmake')
    cache:  # Whether to cache the bootstrap for faster runs (default true)
    cache-path:  # Location of the Procursus cache (default /usr/local/opt/__procursus_cache)

```

If Procursus is already bootstrapped (the file `/opt/procursus/.procursus_strapped` exists), running this action will configure missing environment variables then update and install requested packages.

## Issues
Feel free to submit any issues or pull requests.

## License

This project is released under the [0BSD License](LICENSE)
