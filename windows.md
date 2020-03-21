Windows
=======

VSCode
------

### Backup

```ps
mkdir -ErrorAction SilentlyContinue User\snippets

# Backup settings files
Copy-Item -Path $env:appdata\Code\User\keybindings.json -Destination User
Copy-Item -Path $env:appdata\Code\User\settings.json -Destination User
Copy-Item -Path $env:appdata\Code\User\snippets\* -Destination User\snippets

# Export extension list
code --list-extensions | Out-File -FilePath vscode-extensions.txt
```

### Restore

```ps
# Restore settings files
Get-ChildItem -File User | Copy-Item -Path { $_.FullName } -Destination $env:appdata\Code\User
Get-ChildItem -File User\snippets | Copy-Item -Path { $_.FullName } -Destination $env:appdata\Code\User\snippets

# Import extensions
ForEach ($name in Get-Content vscode-extensions.txt) {
  Write-Host $name -ForegroundColor Blue
  code --install-extension $name
  Write-Host `n
}
```

VSCodium
--------

### Backup

```ps
mkdir -ErrorAction SilentlyContinue User\snippets

# Backup settings files
Copy-Item -Path $env:appdata\VSCodium\User\keybindings.json -Destination User
Copy-Item -Path $env:appdata\VSCodium\User\settings.json -Destination User
Copy-Item -Path $env:appdata\VSCodium\User\snippets\* -Destination User\snippets

# Export extension list
codium --list-extensions | Out-File -FilePath vscode-extensions.txt
```

### Restore

```ps
# Restore settings files
Get-ChildItem -File User | Copy-Item -Path { $_.FullName } -Destination $env:appdata\VSCodium\User
Get-ChildItem -File User\snippets | Copy-Item -Path { $_.FullName } -Destination $env:appdata\VSCodium\User\snippets

# Import extensions
ForEach ($name in Get-Content vscode-extensions.txt) {
  Write-Host $name -ForegroundColor Blue
  codium --install-extension $name
  Write-Host `n
}
```

MrCode
------

### Backup

```ps
mkdir -ErrorAction SilentlyContinue User\snippets

# Backup settings files
Copy-Item -Path $env:appdata\MrCode\User\keybindings.json -Destination User
Copy-Item -Path $env:appdata\MrCode\User\settings.json -Destination User
Copy-Item -Path $env:appdata\MrCode\User\snippets\* -Destination User\snippets

# Export extension list
mrcode --list-extensions | Out-File -FilePath vscode-extensions.txt
```

### Restore

```ps
# Restore settings files
Get-ChildItem -File User | Copy-Item -Path { $_.FullName } -Destination $env:appdata\MrCode\User
Get-ChildItem -File User\snippets | Copy-Item -Path { $_.FullName } -Destination $env:appdata\MrCode\User\snippets

# Import extensions
ForEach ($name in Get-Content vscode-extensions.txt) {
  Write-Host $name -ForegroundColor Blue
  mrcode --install-extension $name
  Write-Host `n
}
```
