# Nushell syntax highlight for sublime text
- Just copied matlab syntax file and modified it for nushell
- Use nushell lsp language server (need lsp sublime package)

# Instalation
1. In sublime text install the LSP package.
2. In nushell (tested in Ubuntu 20.04):
```bash
ls | find -v README & export & color | get name | ansi strip | each {|file| cp -f $file (~/.config/sublime-text/Packages/User/nushell.sublime-syntax | path expand)}
```
3. In sublime, open `Preferences > Customize Color Scheme` and add the contents of `sublime-color-scheme`. Modify to your liking.

# Update commands
If you need to update nushell functions or add your custom commands and aliases, run:
```bash
chmod +x export.nu 
./export.nu 
```