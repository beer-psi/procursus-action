# procursus-action

Bootstraps the Procursus toolchain onto a macOS runner. 

## fuck is Procursus?

[Procursus](https://github.com/ProcursusTeam/Procursus) is a build-system that provides a large set of consistently up-to-date *nix tools cross compiled to work on Darwin based platforms.

## Usage

Only macOS runners, since Procursus itself only compiles for Darwin-based platforms

```bash
- uses: beerpiss/procursus-action@v1

# That's it, there's no other arguments.

```

## Issues

Feel free to submit any issues or pull requests.

### Known issues
- /opt/procursus/bin/dpkg exits with error code 100. Restart workflow, I don't know why this happens /shrug

## License

This project is released under the [0BSD License](LICENSE)
