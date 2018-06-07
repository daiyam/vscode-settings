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

Extensions
----------

- [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
- [colorize](https://marketplace.visualstudio.com/items?itemName=kamikillerto.vscode-colorize)
- [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
- [Docker](https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker)
- [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
- [ignore-gitignore](https://marketplace.visualstudio.com/items?itemName=stubailo.ignore-gitignore)
- [javascript console utils](https://marketplace.visualstudio.com/items?itemName=whtouche.vscode-js-console-utils)
- [Kaoscript Language](https://marketplace.visualstudio.com/items?itemName=kaoscript.kaoscript-language)
- [Line endings](https://marketplace.visualstudio.com/items?itemName=jhartell.vscode-line-endings)
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)
- [Markdown Shortcuts](https://marketplace.visualstudio.com/items?itemName=mdickin.markdown-shortcuts)
- [nginx.conf](https://marketplace.visualstudio.com/items?itemName=shanoor.vscode-nginx)
- [Open a file's folder as Workspace in VS Code](https://marketplace.visualstudio.com/items?itemName=auchenberg.vscode-open-file-folder)
- [open native terminal](https://marketplace.visualstudio.com/items?itemName=alexeyvax.vscode-open-native-terminal)
- [Prettify JSON](https://marketplace.visualstudio.com/items?itemName=mohsen1.prettify-json)
- [Projects+](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-projects-plus)
- [reactstrap-snippets](https://marketplace.visualstudio.com/items?itemName=jjpatel361.reactstrap-snippets)
- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons)
- [Zokugun Theme](https://marketplace.visualstudio.com/items?itemName=zokugun.zokugun-theme)

**Enjoy!**