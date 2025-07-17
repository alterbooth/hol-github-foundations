## ブランチ保護ルールの設定

ブランチ保護ルールの作成について確認する。

- １. `foundations-hands-on-2`リポジトリにgithub.comでアクセスし、ナビゲーションのSettingsにアクセスする
- ２． ルールセットの設定画面から新規ブランチルールセットを作成する
  - `Rules` ＞ `Ruleset` を選ぶ
  - ![ルールセットへ移動](../image/image3-37.png)
  - `New ruleset` ＞ `New branch ruleset` を選ぶ
  - ![ブランチルールの選択](../image/image3-38.png)
- ３． ブランチ保護のルールセットを作成する
  - `Ruleset Name`に`foundations-hands-on-2-ruleset`を入力する
  - ![RulesetName](../image/image3-39.png)
  - `Enforcement status`を`Active`に設定する
  - ![EnforcementStatus](../image/image3-40.png)
  - `Branch targeting criteria`を`Include default branch`に設定する
  - ![BranchTargetingCriteria](../image/image3-41.png)
  - `Require a pull request before merging`をチェック
  - 表示された追加項目内の`Require conversation resolution before merging`をチェック
  - ![PullRequestRule](../image/image3-42.png)
  - ページ下部の、`Create`を押し、ルールセットを作成する
  - 認証が求められる場合があるため、その際は認証する
  - ![PullRequestRule](../image/image3-43.png)
  - `Rulesets`から、ルールセットが作成されていることを確認する
  - ![ルールセットの確認](../image/image3-44.png)