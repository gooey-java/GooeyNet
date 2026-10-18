# GooeyNet

Send messages between classmates' computers and build apps that talk to each
other, like chat apps and multiplayer games. Programs connect through a class
server, so there are no sockets to set up. Part of the
[Gooey Java](https://gooey-java.github.io/) libraries for AP Computer Science A.

**GooeyNet is still in development.** There's no jar to download yet.

**Website:** https://gooey-java.github.io/GooeyNet/

## What's in this repository

| Path | What it is |
|---|---|
| `src/gooeynet/` | The library's source code |
| `GooeyNet.jar` | The compiled library |
| `GooeyNet-sources.jar` | The source code as a jar, for hover docs in VS Code |
| `site/` | The showcase page (the website's home page) |
| `build.sh`, `build.bat` | Build the jars, the Javadoc, and the website |
| `javadoc-options.txt` | Settings for the docs (title, footer, Java version) |
| `.github/workflows/pages.yml` | Publishes the website after every push |
| `LICENSE` | The MIT License |

`src/gooeynet/` is empty for now (its `.gitkeep` file only keeps the folder in
Git). Until code is added there, the build only publishes the showcase page.
Once it has code, the same build also makes the jars and the Javadoc, and the
showcase page will need its download links and a first program added.

## Building and publishing

You need a JDK 17 or newer. Run `./build.sh` (Mac/Linux) or `build.bat`
(Windows). That rebuilds `GooeyNet.jar` and `GooeyNet-sources.jar` in this folder
(compiled to run on Java 17 or newer) and builds the whole website in
`_site/`: the showcase page, the Javadoc in `_site/docs/`, and both jars. Open
`_site/index.html` to preview it. (`_site/` isn't committed; GitHub builds its own.)

Publishing is automatic: after every push to `main`, GitHub runs `build.sh` and
publishes `_site/` to https://gooey-java.github.io/GooeyNet/. The **Actions** tab
on GitHub shows each run. This needs a one-time setting: **Settings > Pages >
Source: GitHub Actions**.

The showcase page is `site/index.html`. Its styles come from
`https://gooey-java.github.io/gooey.css` in the gooey-java.github.io repo, which
every Gooey Java page shares.

## License

GooeyNet is released under the [MIT License](LICENSE): anyone may use, copy,
change, and share it, as long as the copyright notice and license are kept with it.
