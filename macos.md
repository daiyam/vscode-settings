Linux
=====

VSCode
------

### Backup

```
mkdir -p User/snippets

# Backup settings files
cp ~/Library/Application\ Support/Code/User/keybindings.json User/
cp ~/Library/Application\ Support/Code/User/settings.json User/
cp ~/Library/Application\ Support/Code/User/snippets/* User/snippets/

# Export extension list
code --list-extensions | sort -f -o vscode-extensions.txt
```

### Restore

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

VSCodium
--------

### Backup

```
mkdir -p User/snippets

# Backup settings files
cp ~/Library/Application\ Support/VSCodium/User/keybindings.json User/
cp ~/Library/Application\ Support/VSCodium/User/settings.json User/
cp ~/Library/Application\ Support/VSCodium/User/snippets/* User/snippets/

# Export extension list
codium --list-extensions | sort -f -o vscode-extensions.txt
```

### Restore

```
# Restore settings files
cp User/* ~/Library/Application\ Support/VSCodium/User/

# Import extensions
for LINE in $(cat "vscode-extensions.txt")
do
  printf "%b%s%b\n" "\e[44m" "$LINE" "\e[49m"
  codium --install-extension "$LINE"
  echo -e "\n"
done
```

MrCode
------

### Backup

```
mkdir -p User/snippets

# Backup settings files
cp ~/Library/Application\ Support/MrCode/User/keybindings.json User/
cp ~/Library/Application\ Support/MrCode/User/settings.json User/
cp ~/Library/Application\ Support/MrCode/User/snippets/* User/snippets/

# Export extension list
mrcode --list-extensions | sort -f -o vscode-extensions.txt
```

### Restore

```
# Restore settings files
cp User/* ~/Library/Application\ Support/MrCode/User/

# Import extensions
for LINE in $(cat "vscode-extensions.txt")
do
  printf "%b%s%b\n" "\e[44m" "$LINE" "\e[49m"
  mrcode --install-extension "$LINE"
  echo -e "\n"
done
```
