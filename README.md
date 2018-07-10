[daiyam/vscode-settings](https://github.com/daiyam/vscode-settings)
===============================================================

Provides my preferred settings for vscode

[Follow the documentation to install the command `code`](https://code.visualstudio.com/docs/setup/setup-overview)

VSCode
------

### Backup

```
mkdir User

# Backup settings files
cp ~/Library/Application\ Support/Code/User/keybindings.json User/
cp ~/Library/Application\ Support/Code/User/settings.json User/

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

Code OSS
--------

### Backup

```
mkdir User

# Backup settings files
cp ~/Library/Application\ Support/Code\ OSS/User/keybindings.json User/
cp ~/Library/Application\ Support/Code\ OSS/User/settings.json User/
```

### Restore

```
# Restore settings files
cp User/* ~/Library/Application\ Support/Code\ OSS/User/
```

Extensions
----------

- [Better TOML](https://marketplace.visualstudio.com/items?itemName=bungcip.better-toml)
- [colorize](https://marketplace.visualstudio.com/items?itemName=kamikillerto.vscode-colorize)
- [Copy filename](https://marketplace.visualstudio.com/items?itemName=jack89ita.copy-filename)
- [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
- [Docker](https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker)
- [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [ignore-gitignore](https://marketplace.visualstudio.com/items?itemName=stubailo.ignore-gitignore)
- [Kaoscript Language](https://marketplace.visualstudio.com/items?itemName=kaoscript.kaoscript-language)
- [Line endings](https://marketplace.visualstudio.com/items?itemName=jhartell.vscode-line-endings)
- [Live Server Preview](https://marketplace.visualstudio.com/items?itemName=negokaz.live-server-preview)
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)
- [Markdown Shortcuts](https://marketplace.visualstudio.com/items?itemName=mdickin.markdown-shortcuts)
- [nginx.conf](https://marketplace.visualstudio.com/items?itemName=shanoor.vscode-nginx)
- [Open a file's folder as Workspace in VS Code](https://marketplace.visualstudio.com/items?itemName=auchenberg.vscode-open-file-folder)
- [open native terminal](https://marketplace.visualstudio.com/items?itemName=alexeyvax.vscode-open-native-terminal)
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Prettify JSON](https://marketplace.visualstudio.com/items?itemName=mohsen1.prettify-json)
- [Projects+](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-projects-plus)
- [Pug Template Literals](https://marketplace.visualstudio.com/items?itemName=zokugun.vscode-pug-template-literal)
- [TSLint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint)
- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons)
- [Zokugun Theme](https://marketplace.visualstudio.com/items?itemName=zokugun.zokugun-theme)

**Enjoy!**