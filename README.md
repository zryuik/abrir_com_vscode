


# 💻 VS Code: Atalhos de Contexto (Windows)

Esta funcionalidade adiciona atalhos no menu de contexto do Windows, permitindo que pastas e arquivos possam ser abertos diretamente no Visual Studio Code.

Os arquivos de registro abaixo foram configurados com o caminho de instalação: **`D:\vsssscode\Microsoft VS Code\Code.exe`**.

-----

## Como Usar

Para adicionar qualquer um dos atalhos, siga estes passos simples:

1.  Crie um novo arquivo de texto, cole o código do atalho desejado e salve-o com a extensão **`.reg`** (ex: `atalho.reg`).
2.  **Dê um duplo clique** no arquivo `.reg` e confirme as alterações para que as chaves sejam adicionadas ao Registro do Windows.

-----

## 1\. Atalho para Abrir Arquivos

Adiciona a opção para abrir **arquivos individuais** (ao clicar com o botão direito **em cima de um arquivo**).

```ini
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\*\shell\VSCodeFile]
@="Abrir com VSCode"
"Icon"="\"D:\\vsssscode\\Microsoft VS Code\\Code.exe\""

[HKEY_CLASSES_ROOT\*\shell\VSCodeFile\command]
@="\"D:\\vsssscode\\Microsoft VS Code\\Code.exe\" \"%1\""
```

## 2\. Atalho para Abrir Pastas

Adiciona a opção para abrir **pastas** (ao clicar com o botão direito **em cima do ícone da pasta**).

```ini
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\shell\VSCodeDirectory]
@="Abrir com VSCode"
"Icon"="\"D:\\vsssscode\\Microsoft VS Code\\Code.exe\""

[HKEY_CLASSES_ROOT\Directory\shell\VSCodeDirectory\command]
@="\"D:\\vsssscode\\Microsoft VS Code\\Code.exe\" \"%V\""
```

## 3\. Atalho para Abrir na Pasta Atual

Adiciona a opção para abrir a **pasta atual** (ao clicar com o botão direito **na área vazia dentro de uma pasta**).

```ini
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\Background\shell\VSCodeBackground]
@="Abrir com VSCode"
"Icon"="\"D:\\vsssscode\\Microsoft VS Code\\Code.exe\""

[HKEY_CLASSES_ROOT\Directory\Background\shell\VSCodeBackground\command]
@="\"D:\\vsssscode\\Microsoft VS Code\\Code.exe\" \".\""
```
