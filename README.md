# procursus-action
Bootstraps the Procursus toolchain onto a macOS runner. 

## fuck is Procursus?
[Procursus](https://github.com/ProcursusTeam/Procursus) is a build-system that provides a large set of consistently up-to-date *nix tools cross compiled to work on Darwin based platforms.

## Usage
Only macOS 11 and newer runners (`macos-latest`), since Procursus itself only compiles for Darwin-based platforms.

```yaml
- uses: beerpiss/procursus-action@v1  # the v1 tag refers to the latest of major version 1 (currently 1.4)
  with:
    packages:  # A space-delimited list of what to install after bootstrapping (etc. 'clang cmake')
    cache:  # Whether to cache the bootstrap for faster runs (default: true)
    cache-path:  # Location of the Procursus cache (default: /usr/local/opt/__procursus_cache)
    mirror:  # URL of Procursus repository (default: https://apt.procurs.us)
    suites:  # Suites to use (default: big_sur) 
    components:  # Components to use (default: main)
```

If Procursus is already bootstrapped (the file `/opt/procursus/.procursus_strapped` exists), running this action will configure missing environment variables then update and install requested packages.

## Issues
Feel free to submit any issues or pull requests.

## License

This project is released under the [0BSD License](LICENSE)
