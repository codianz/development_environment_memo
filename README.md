# CODIANZ での開発環境構築メモ

## Node.js

### Windows

* https://nodejs.org/en/ よりインストール
* 12.16.1 LTS
* WSL を使う方法もアリ

### MacOS

#### Homebrew をインストール

http://brew.sh/index_ja.html

```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### nodebrew をインストール

```sh
brew install nodebrew
```

#### Node.js をインストール

``` sh
mkdir -p ~/.nodebrew/src
nodebrew ls-remote        # バージョン一覧を取得
nodebrew install-binary バージョン # バージョン例（v12.16.1）
nodebrew use バージョン   # バージョン例（v12.16.1）
echo 'export PATH=$HOME/.nodebrew/current/bin:$PATH' >> ~/.zprofile
```

### 共通

#### npm-check-updates をインストール

```sh
npm i npm-check-updates -g
```

#### Vue.js をインストール

```sh
npm i @vue/cli -g
```

## Visual Studio Code （VSCode）

### VSCode をインストール

https://code.visualstudio.com/download


### 機能拡張をインストール

#### 必須

* Debugger for Chrome
* ESLint
* Live Server
* Vetur
* REST Client
* Git History
* Git Lens

#### 任意

* Remove-WSL （Windowsのみ）

### VScode 設定

```json
{
  "editor.tabSize": 2,
  "window.restoreWindows": "none"
}
```

## Git

### 共通

#### Sourcetree をインストール

https://www.sourcetreeapp.com/


### Windows

#### git for windows をインストール

Sourcetree と併せて、下記もインストールする。

https://gitforwindows.org/

インストール後に念のため下記のコマンドを実施する。

```sh
git config --global core.autocrlf false
```


