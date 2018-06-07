[daiyam/vscode-settings](https://github.com/daiyam/vscode-settings)
===============================================================

Provides my preferred settings for vscode

[Follow the documentation to install the command `code`](https://code.visualstudio.com/docs/setup/setup-overview)

Backup
------

```
mkdir User

# Backup settings files
cp ~/Library/Application\ Support/Code/User/keybindings.json User/
cp ~/Library/Application\ Support/Code/User/settings.json User/

# Export extension list
code --list-extensions | sort -f -o vscode-extensions.txt
```

Restore
-------

```
# Restore settings files
cp User/* ~/Library/Application\ Support/Code/User/

# Import extensions
for LINE in $(cat "vscode-extensions.txt")
do
  printf "%b%s%b\n" "\e[44m" "$LINE" "\e[49m"
  code --install-extension "$LINE"
  echo -e "\n"
done
```

**Enjoy!**