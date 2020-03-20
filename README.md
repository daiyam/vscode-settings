[daiyam/vscode-settings](https://github.com/daiyam/vscode-settings)
===================================================================

Provides my preferred settings for vscode

[Follow the documentation to install the command `code`](https://code.visualstudio.com/docs/setup/setup-overview)

Backup
------

```
mkdir -p User/snippets

# Backup settings files
cp ~/Library/Application\ Support/Code/User/keybindings.json User/
cp ~/Library/Application\ Support/Code/User/settings.json User/
cp ~/Library/Application\ Support/Code/User/snippets/* User/snippets/

# Export extension list
code --list-extensions | sort -f -o vscode-extensions.txt
```

Restore
-------

```
# Restore settings files
cp -r User/* ~/Library/Application\ Support/Code/User/

# Import extensions
for LINE in $(cat "vscode-extensions.txt")
do
  printf "%b%s%b\n" "\e[44m" "$LINE" "\e[49m"
  code --install-extension "$LINE"
  echo -e "\n"
done
```

Binary Names
------------

- __VSCode__: `code`
- __VSCodium__: `codium`
- __MrCode__: `mrcode`

Settings Paths
--------------

### VSCode

- __Windows__: `%APPDATA%\Code\User`
- __macOS__: `~/Library/Application Support/Code/User`
- __Linux__: `~/.config/Code/User`

### VSCodium

- __Windows__: `%APPDATA%\VSCodium\User`
- __macOS__: `~/Library/Application Support/VSCodium/User`
- __Linux__: `~/.config/VSCodium/User`

### MrCode

- __Windows__: `%APPDATA%\MrCode\User`
- __macOS__: `~/Library/Application Support/MrCode/User`
- __Linux__: `~/.config/MrCode/User`


**Enjoy!**