---
marp: true
---

# Rパッケージ開発入門

## 第13章：GitとGitHub

担当：福井

---
## Git・GitHubとは

GitとGitHubをつかったパッケージ管理は便利

- Git：バージョン管理システムの一つ
  - コードの変更が追跡可能
- GitHub：コードを共有するwebサービス
  - pull requestで改善案を申請し、課題を管理可能

---
## Git/GitHubをつかって開発したパッケージを利用する

GitHubを使えば以下の方法で誰でもRパッケージを利用（インストール）できる
  
```
install.package("devtools")
devtools::install_github("ichimomo/frasyr") 
# (""のなかは、GitHubのusername/package名)
```
- GitHubのパッケージのサイトでコードを読むこともできるしMarkdown形式で書かれたドキュメントを参照できる
- Issueをつかってバグレポートできる

---
## 13.1 RstudioとGit、GitHub

Consoleだけじゃなくて、Treminalでも操作してみて

- ちょっとだけLinuxのterminal操作（シェルコマンド）を知っておくと良い
- 例えば
  - pwd （カレントディレクトリの表示）
  - cd　（ディレクトリの移動）
  - ls　（カレントディレクトリ下のファイル表示）

---
## 13.2 初期設定

1. Gitインストール（全員完了したものとする）
2. Gitユーザー名とメールアカウント設定（全員完了したものとする）
3. GitHubアカウント作成（全員完了したものとする）
4. SSH鍵作成　（やらないと通信で毎回パスワード聞かれる）
- 鍵があるかどうかは以下のコマンドで確認可能
```
file.exists("~.ssh/id_rsa.pub")
```

----
## 13.3 ローカルのGitリポジトリ作成
