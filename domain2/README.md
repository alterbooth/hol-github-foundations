# ドメイン2:GitHubリポジトリの操作

## リポジトリのナビゲーション

リポジトリのナビゲーションを確認する。

- １. 先ほど作成した`foundations-hands-on-1`リポジトリをgithub.comで開く
- ２. ブランチの選択やファイルの一覧があり、READMEやLICENSEが表示されている事を確認する
- ３. 画面右側にリポジトリの各種メタ情報が表示されていることを確認する

## テンプレートリポジトリ

テンプレートリポジトリについて確認する。

- １. `foundations-hands-on-1`リポジトリのナビゲーションのSettingsにアクセスする
- ２. Generalの`Template repository`にチェックを入れる
  - ![Template repository](../image/image2-1.png)
- ３. ナビゲーションのCodeで、右上の「Use this template」を押して、テンプレートから`foundations-hands-on-2`という新しいパブリックリポジトリを作成する
  - ![Use this template](../image/image2-2.png)

## ブランチの作成

github.com上でのブランチの作成方法を確認する。

- １. `foundations-hands-on-2`リポジトリにgithub.comでアクセスし、ナビゲーションのCodeでブランチ選択のプルダウンを開き、「Switch branches/tags」の下の枠に`update-readme-2`と入力し、「Create branch update-readme-2 from main」を選択して`update-readme-2`ブランチを作る
  - ![Create a branch](../image/image2-3.png)

## ファイルの追加

github.com上でのファイルの追加方法を確認する。

- １. ナビゲーションのCodeから「Add file」ボタンを押してファイルを作成する
  - ![Add file](../image/image2-4.png)
    - (*)ウインドウのサイズなどによって「Add file」ボタンが「＋」ボタンになっている場合がある
  - ファイル名に`.github/README.md`と入力
  - ![input file name](../image/image2-5.png)
  - 本文に`# foundations-hands-on-2`と入力してコミットする
  - ![変更内容をコミット](../image/image2-9.png)
- ２. ナビゲーションのCodeで、今作ったファイルがREADMEとして表示されていることを確認する
  - これによって、複数のREADMEがある場合、`.github`ディレクトリ -> rootディレクトリ -> `docs`ディレクトリの順で優先的に表示されるようになっていることが分かる
  - 時間があるならファイルを削除したり、`docs/README.md`を作成してみて、複数のREADMEがある場合の動作を詳細に確認する
  - 参考：[READMEについて](https://docs.github.com/ja/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
- ３. 他のファイルについては[公式ドキュメント](https://docs.github.com/ja/enterprise-cloud@latest/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository)を確認しておく

## ファイルの削除
- １. ナビゲーションのCodeから、削除対象のファイルを選択する
  - 先ほど作成した`.github/README.md`を選択する
  - ![.githubフォルダを選択](../image/image2-10.png)
  - ![README.mdを選択](../image/image2-11.png)
- ２． ファイルを削除する
  - 画面右上の`・・・`から`Delete file`を選択する
  - ![README.mdを削除](../image/image2-13.png)
- ３． 削除の変更をコミットする
  - ![README.mdの削除をコミット](../image/image2-14.png)
- ４． `.github/README.md`が削除されたことを確認する
  - ![README.mdの削除を確認](../image/image2-15.png)

## starを付ける

Starについて確認する。

- １. [Visual Studio Codeのリポジトリ](https://github.com/microsoft/vscode)にアクセス
  - starを押してみる
  - ![star](../image/image2-6.png)
- ２. [https://github.com/stars](https://github.com/stars)にアクセスしてみると、vscodeが出てくるのを確認する
- ３. Visual Studio Codeのリポジトリに戻って、[画面右のメタデータのstars](https://github.com/microsoft/vscode/stargazers)を見てみると、starを付けたアカウントが見られることを確認する

## Feature preview

github.comの任意の画面からアカウントアイコンをクリックし、メニューから「Feature preview」にアクセスしてみる。

![account icon](../image/image2-7.png)

![Feature preview](../image/image2-8.png)

---
[前ドメインへ](../domain1/README.md)  
[次のドメインへ](../domain3/README.md)  
[目次へ](../README.md)
