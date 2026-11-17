# prac — practical code loader

Students type one command in any terminal, pick a practical number, and the full
code is printed in that same terminal, copied to the clipboard, and saved as a file.

| Where | Command |
|---|---|
| Windows PowerShell | `irm https://swastik-4752.github.io/prac/w.txt \| iex` |
| Windows cmd | `powershell -c "irm https://swastik-4752.github.io/prac/w.txt \| iex"` |
| Linux / macOS / Git Bash | `curl -fsSL https://swastik-4752.github.io/prac/l.txt \| bash` |
| Any terminal, no menu | `curl -fsSL https://swastik-4752.github.io/prac/2.txt` (prints practical 2; use `curl.exe` in PowerShell) |
| Install `prac` on Windows (once) | `irm https://swastik-4752.github.io/prac/install.txt \| iex` → then `prac` or `prac 2` |

Linux/macOS shortcut: add to `~/.bashrc` → `alias prac='curl -fsSL https://swastik-4752.github.io/prac/l.txt | bash -s'`

## Files

| File | What it is |
|---|---|
| `list.txt` | The menu: `number \| title \| file name it is saved as` |
| `1.txt`, `2.txt`, … | The code for each practical |
| `w.txt` | Windows loader (PowerShell) |
| `l.txt` | Linux / macOS loader (bash) |
| `install.txt` | Puts a `prac.cmd` on the Windows PATH |
| `index.html` | Web page with copy buttons and the practical list |

## Adding a practical

1. Put the code in `9.txt` (next free number; `1.txt` is also free).
2. Add a line to `list.txt`: `9 | Title of practical | practical9_name.txt`
3. Push to GitHub. Students get it on their next run — nothing to reinstall.

## Hosting (free, GitHub Pages)

Live at https://swastik-4752.github.io/prac (GitHub Pages, `main` branch, root).
A push to `main` updates the site in about a minute.

To host it on another account: replace `https://swastik-4752.github.io/prac` in `w.txt`,
`l.txt`, `install.txt` and this README with `https://<github-username>.github.io/prac`
(lowercase username), push to a public repo named `prac`, then
Settings → Pages → Deploy from branch → `main` / root.
