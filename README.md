# ZrnSelectiveSuspend website

The landing page and wiki for [ZrnSelectiveSuspend](https://github.com/z3r0n3br4instorm/ZrnSelectiveSuspend),
as one static page for GitHub Pages. No build step.

```
index.html                    the whole site: landing, wiki, styles and script
assets/macbook-pro-2012.png   the "Tested on" picture
.nojekyll                     serve the files as they are
```

## Publishing on GitHub Pages

It is published from the repository `Zerone-Laboratories/zss`, at
`https://zerone-laboratories.github.io/zss/`. From this folder, once:

```sh
git init -b main
git add .
git commit -m "website"
gh repo create Zerone-Laboratories/zss --public --source . --push
gh api -X POST repos/Zerone-Laboratories/zss/pages -f "source[branch]=main" -f "source[path]=/"
```

The last line is the same as **Settings → Pages → Deploy from a branch**, branch `main`,
folder `/ (root)`. The site appears a minute or so later, and every later push republishes it.
The repository has to be public for Pages on GitHub's free plan.

A domain of your own: add a file `CNAME` holding the name (for example `zss.example.org`),
point that name's DNS at `zerone-laboratories.github.io` with a CNAME record, and enter it
under **Settings → Pages → Custom domain**.

## The install command

The title bar and the Install section download
`https://github.com/z3r0n3br4instorm/ZrnSelectiveSuspend/releases/latest/download/zss-installer.run`.
That name exists from the first release built by the project's workflow after the
change that adds the unversioned copies (`zss-installer.run`, `zss-tester.run`) to each release.

## Style

Hairline mono: greyscale only, square corners, 1 px borders, no shadows or gradients,
Archivo in light weights, a 120 ms colour change as the only motion. Dark mode follows the
device and has a toggle in the sidebar. Australian spelling.
