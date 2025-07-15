# ドメイン1:GitとGitHubの紹介

## リポジトリの作成

[github.com](https://github.com)で、自身のアカウントにパブリックなリポジトリを作成する。  
本ドキュメントを参照しながら作業できるように、ブラウザの別のタブまたは別のウインドウで開いて作業する。

- １. 以下のボタンを押して、新しいリポジトリの作成画面に移動する
  - ![create new repository](../image/image1-2.png)  
- ２. リポジトリの作成画面で、次の項目を設定し、リポジトリを作成する
  - 「Repository template」は「No template」を選択する
  - 「Owner」は自分のアカウントを選ぶ(選択肢がある場合)
  - 「Repository name」は`foundations-hands-on-1`と入力
  - 「Public」を選択
  - 「Initialize this repository with:」は以下のように選択する
    - 「Add a README file」にチェックを入れる
    - 「Add .gitignore」は「.gitignore template: None」を選択する
    - 「Choose a license」は「MIT License」を選択する
  - ![repository settings](../image/image1-3.png)

## リポジトリのクローンとgitの操作

自身のPCにクローンして、gitの基本操作を行ってみる。

- １. 事前にインストールしていたVisual Studio Codeを起動する
  - 「ターミナル」メニューから「新しいターミナル」を選択する
  - ![新しいターミナル](../image/image1-4.png)
  - Visual Studio Codeの画面下部に、ターミナル(文字でコマンドを入力して作業を行う場所)が表示される
  - ![ターミナル](../image/image1-5.png)
- ２. ターミナルで、gitの初期設定を行う（※後述）
  - `git config --global user.name "あなたの名前"`コマンドを実行する
  - `git config --global user.email "あなたのgithubのアカウントのメールアドレス"`コマンドを実行する
    - (*)`--global`オプションをつけると、この設定があなたのPCのアカウント全体に適用される。この設定を特定のリポジトリだけに適用したい場合は、後述のクローンしたディレクトリに移動した（★）あとに、`--global`オプションを付けずに実行する。
- ３. ブラウザで開いているgithub.comのリポジトリのページで、ナビゲーションのCodeを開き、「Code」ボタンからHTTPSのURLをコピーする
  - ![URLをコピー](../image/image1-1.png)
- ４. ターミナルで`git clone 取得したURL`コマンドを実行する。このコマンドを実行すると、ターミナルで開いているディレクトリに`foundations-hands-on-1`というディレクトリが作成され、その中にリポジトリのファイルがクローンされる
- ５. ターミナルで`cd foundations-hands-on-1`コマンドを実行し、リポジトリのディレクトリに移動する（★）
- ６. 作業用ブランチを作成する
  - ターミナルで`git branch`コマンドを実行し、現在は`main`ブランチにいることを確認する
  - ターミナルで`git switch -c update-readme`コマンドを実行する
  - ターミナルで`git branch`コマンドを実行し、作成した`update-readme`ブランチにいることを確認する
- ７. `README.md`を編集する
  - Visual Studio Codeのファイルメニューから「ファイルを開く」を選択し、`foundations-hands-on-1`ディレクトリにある`README.md`を開く
  - ![ファイルを開く](../image/image1-6.png)
  - 適当な文字列を追加して、保存する
- ８. 状態を確認する
  - ターミナルで`git status`コマンドを実行する
  - 変更されたファイルが1つあり、ステージされていないというメッセージが出るのを確認する
- ９. 変更したファイルをステージングエリアに追加する
  - ターミナルで`git add README.md`コマンドを実行する
- １０. 状態を確認する
  - ターミナルで`git status`コマンドを実行する
  - 変更されたファイルが1つあり、ステージされているというメッセージが出るのを確認する
- １１. ステージングエリアのファイルをコミットする
  - ターミナルで`git commit -m "[modify] update README"`コマンドを実行する
- １２. リモートリポジトリにプッシュする
  - ターミナルで`git push --set-upstream origin update-readme`コマンドを実行する
    - (*)手元で作成したブランチをリモートリポジトリに作成する場合、`--set-upstream`オプションを付ける必要がある
- １３. github.comでリポジトリにアクセスし、ファイルが変更されているのを確認する
  - 一度画面をリロードする
  - ナビゲーションのCodeの、「Code」タブの下にブランチを選択できるプルダウンがあるので、ここから`update-readme`を選択する
  - ![ブランチの選択](../image/image1-7.png)
- １４. 画面上から`README.md`を変更する(鉛筆ボタンを押す)
  - ![鉛筆ボタン](../image/image1-8.png)
  - 資料で説明されたmarkdownを色々書いてみる
  - [公式ドキュメント](https://docs.github.com/ja/enterprise-cloud@latest/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
  - 変更内容を直接コミットする
  - ![変更内容をコミット](../image/image1-9.png)
  - `README.md`の変更履歴を確認する
  - コミット後の画面で、`History`を押す
  - ![変更内容の確認1](../image/image1-10-a.png)
  - 変更履歴を確認する
  - ![変更内容の確認2](../image/image1-10-b.png)
- １５. 画面で変更したものをローカルのリポジトリに反映する
  - Visual Studio Codeのターミナルで`git pull`コマンドを実行する
  - `README.md`が変更されているのを確認する
  - ターミナルで`git log`コマンドを実行する
  - ローカルの変更履歴を確認する

※ Gitの初期設定（`git config`）についての詳細は、[Gitの初期設定](https://git-scm.com/book/ja/v2/%e4%bd%bf%e3%81%84%e5%a7%8b%e3%82%81%e3%82%8b-%e6%9c%80%e5%88%9d%e3%81%aeGit%e3%81%ae%e6%a7%8b%e6%88%90)の「個人の識別情報」をご参照ください。

## リポジトリの初期化

リポジトリの初期化を行ってみる。

- １. GitHub Codespacesを起動する
  - [Codespacesのテンプレート選択ページ](https://github.com/codespaces/templates) にアクセスし、`Blank`を選択する。
  - ![Codespacesテンプレート選択](../image/image1-11.png)
  - 起動したCodespacesのターミナルが表示されていることを確認する
  - ![Codespacesターミナル](../image/image1-12.png)
- ２． リポジトリとなるディレクトリを作成する
  - ターミナルで`mkdir test-repository`コマンドを実行し、`test-repository`ディレクトリを作成する
  - ターミナルで`cd test-repository`コマンドを実行し、作業ディレクトリを変更する
- ３． リポジトリを初期化する
  - ターミナルで`git init`コマンドを実行し、リポジトリを初期化する
  - ターミナルで`ls -d .git`コマンドを実行し、`.git`ディレクトリが存在するかを確認する
  - ターミナルで`ls .git`コマンドを実行し、`HEAD` `config` `description` などのファイルが存在するかを確認する
- ４． 変更を加え、gitのコントロール下にあるかを確認する
  - ターミナルで`echo "# test-repository" > README.md`コマンドを実行し、`README.md`ファイルを作成する
  - 画面左部メニューの「ソース管理」を選択し、先ほど作成した`README.md`の変更が追跡されているかを確認する
  - ![Codespacesソース管理](../image/image1-13.png)
- ５． 変更したファイルをステージングエリアに追加する
  - ターミナルで`git add README.md`コマンドを実行する
- ６. ステージングエリアのファイルをコミットする
  - ターミナルで`git commit -m "initial commit"`コマンドを実行する
- ７． 変更履歴を確認する
  - ターミナルで`git log`コマンドを実行し、変更履歴を確認する

## GitHub Desktop

インストール可能ならば、GitHub Desktopをインストールして動かしてみる。
  
- １. [GitHub Desktopのインストール方法](https://docs.github.com/ja/enterprise-cloud@latest/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop)

## GitHub Mobile

インストール可能ならば、GitHub Mobileをインストールして動かしてみる。

---
[次のドメインへ](../domain2/README.md)  
[目次へ](../README.md)
