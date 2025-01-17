# ドメイン5:プロジェクト管理

## Projectsによるプロジェクト管理

Projectsを使ったプロジェクト管理について確認する。併せてLabelsとMilestonesについても確認する。

- github.comで、以下のいずれかからProjects一覧を表示し、「+ New project」ボタンを選択する
  - 任意のリポジトリ（ドメイン1で作成した`foundations-hands-on-1`リポジトリなど）のナビゲーションのProjectsを選択する
    ![リポジトリのProjects一覧を開き、新しいprojectを作成する](../image/image5-1.png)
  - 自身のプロフィールページのナビゲーションのProjectsを選択する
    ![プロフィールページからProjects一覧を開き、新しいprojectを作成する](../image/image5-new-project-from-projects-page.png)
  - 右上のアイコンからメニューを表示し、「Your projects」を選択する  
    <img src="../image/image5-open-your-projects.jpg" alt="プロフィールのメニューから「Your projects」を選択し、Projects一覧を表示する" width="200">
- テンプレートが複数あることを確認する
- ここでは、「Start from scratch」から「Table」を選択する
  ![start from scratch](../image/image5-2.png)
- 「Project name」に`foundations test`と入力し、「Create project」ボタンを選択する
- ドメイン4で作成したリポジトリ`hol-javascript-calculator`でIssueを2つ作る
  - それぞれのIssueで、右の「Projects」の歯車アイコンから、Project「foundations test」に紐付ける  
    <img src="../image/image5-3.png" alt="IssueをProjectに紐づける" width="400">
    - Issueに紐付けられたProjectは、次の図のように表示される
      ![issueに紐付けられたProject](../image/image5-project-displayed-in-issue.png)

ProjectのTableレイアウトとBoardレイアウトのビューの見え方を確認する。

- すでに作成されているTableレイアウトのビューを確認する
  ![ProjectのTableレイアウトのビュー](../image/image5-project-table-layout-view.png)
- 「+ New view」を選択し、「Layout」から「Board」を選択し、Boardレイアウトのビューを作成する  
  <img src="../image/image5-project-new-view-select-board.jpg" alt="Projectの「New view」を選択し、「Board」レイアウトを選択する" width="400">
- 作成したBoardレイアウトのビューを確認する
  ![ProjectのBoardレイアウトのビュー](../image/image5-project-board-layout-view.jpg)
- Boardレイアウトのビューで、アイテム（Issue）をドラッグアンドドロップして「No Status」から「Todo」に移動する
  - 移動したIssueを確認し、Issueの「Project」の状態（この場合はStatus）が反映されていることを確認する
  ![issue側でもprojectの状態が反映される](../image/image5-project-displayed-in-issue-status-changed.png)
- ProjectのBoardレイアウトのビューで、アイテムを「Done」に移動する
  - StatusをDoneに変えると、紐付けたIssueが自動でCloseされることを確認する
    ![ProjectのStatusがDoneに変わると、紐付いたIssueがCloseされる](../image/image5-make-issue-assosicated-project-done.png)

ProjectのWorkflowsで自動化のフローを確認する。

- Project画面右の三点リーダーの「Workflows」を開く
  ![workflows](../image/image5-4.png)
- 組み込みのワークフローについて確認する
  - 例えば、デフォルトで有効になっているItem closedのワークフローにより、StatusをDoneに変更すると紐付けられたIssueがCloseされる

Projectでアイテムを追加してみる。

- Tableレイアウトのビューで、一覧の最後尾の「+」を選択する
  ![add an item](../image/image5-5.png)
  - 「+」ボタンからの操作では、Issueを作成するか、既存のIssueを追加するかが選べることを確認する
- 「+」ボタンの横のテキストフィールドに何か入力する
  - この操作では、draft状態で作るか、Issueを作成するか、既存のIssueを追加するかが選べることを確認する
- draftを作成する
  - 作成したdraftは、Issueに紐付いていないことを確認する
- 作成したdraftを「Convert to issue」でIssueに変換してみる

フィールドを追加してみる。ここでは、Tableレイアウトのビューから、イテレーションフィールドを追加する。

- Tableレイアウトのビューで、一覧の右端の「+」を選択し、「+ New field」を選択する
  ![一覧の右端の「+」を選択し、「+ New field」を選択する](../image/image5-6.png)
- 「Field name」を`Iteration`に変更し、「Field type」を「Iteration」に変更する
  ![「Field name」を`Iteration`に変更し、「Field type」を「Iteration」に変更する](../image/image5-7.png)
- 「Options」の「Starts on」と「Duration」を操作し、イテレーションの開始日と期間を設定する
  ![「Options」の「Starts on」と「Duration」を操作し、イテレーションの開始日と期間を設定する](../image/image5-8.png)
- 現在アイテムが2つ見えているはずなので、それぞれ別のイテレーションを設定する
  - ![set iteration](../image/image5-9.png)
- ビューのタブのプルダウンから、「Group by」で「Iteration」を指定し、イテレーション毎にまとめてみる
  ![group by iteration](../image/image5-10.png)
- Iteration以外のタイプのフィールドも追加できることを確認する

IssuesのLabelがProjectでも利用できることを確認する。

- `hol-javascript-calculator`リポジトリのナビゲーションからIssuesを開き、「Labels」を選択し、Labels一覧を表示する
  ![Labels一覧を表示する](../image/image5-11.png)
- 「New label」ボタンを選択し、「Label name」を入力して、「Create label」ボタンを選択する
  ![「New label」ボタンから、ラベルを作成する](../image/image5-create-new-label.png)
- Issueに作成したラベルを設定する
  ![Issueに作成したラベルを設定する](../image/image5-add-label-to-issue.png)
- Issueをラベルで検索してみる
  ![Issueをラベルで検索してみる](../image/image5-filter-issues-by-label.png)
- Projectsの画面に戻り、Tableレイアウトのビューで「Labels」フィールドを表示する
  ![Tableレイアウトのビューで「Labels」フィールドを表示する](../image/image5-project-display-labels-fields.png)

IssuesのMilestonesがProjectsでも利用できることを確認する。

- `hol-javascript-calculator`リポジトリのナビゲーションのIssuesから、「Milestones」を選択し、Milestones一覧を表示する
  ![add a milestone](../image/image5-12.png)
- 「New Milestone」ボタンを選択する
  ![「New Milestone」ボタンを選択する](../image/image5-new-milestone.png)
- 「Title」に任意の文字列を入力し、「Due date」に本日の日付を指定して、「Create milestone」ボタンを選択してMilestoneを作成する
  ![Titleを入力し、Milestoneを作成する](../image/image5-create-new-milestone.png)
- 2つのIssueにそれぞれMilestoneを設定する
  > [!TIP]
  > Issueのうち1つはcloseされているはずなので、フィルタの`is:open`を削除してすべて表示させるか、一覧上部の「✓ 1 Closed」を選択して、CloseしたIssues一覧を表示して作業を進める
  - IssueにMilestoneを紐付ける
    ![IssueにMilestoneを紐付ける](../image/image5-associate-milestone-to-issue.png)
- Milestoneを確認すると進捗50％になってること確認する
  ![Milestoneの進捗が50%を示している](../image/image5-milestone-progress-shows-50.png)

ProjectのRoadmapレイアウトのビューの見え方を確認する。

- Projectに戻り、Roadmapレイアウトのビューを作成する
  ![ProjectでRoadmapレイアウトのビューを作成する](../image/image5-project-new-view-select-roadmap.png)
- 「Markers」に「Milestone」を指定する
  ![「Markers」に「Milestone」を指定する](../image/image5-project-set-milestone-as-marker-in-roadmap.png)
- Issuesに紐付けたMilestoneがMarkerとして表示されることを確認する
  ![Issuesに紐付けたMilestoneがMarkerとして表示される](../image/image5-milestone-shown-as-marker-in-roadmap.png)

Project Insightsを見てみる。

- Project画面の右のグラフのアイコンを選択する
  ![Project Insightsを開く](../image/image5-open-project-insights.png)
- Project InsightsのDefault chartsやCustom chartsを確認する
  ![Project Insightsの画面](../image/image5-project-insights.png)

Projectのテンプレートを確認する（講師によるデモ）。

- Projectのテンプレートを新しく作成する
  - OrganizationのナビゲーションからProjectsを開き、左の「Templates」を開き、「New template」を選択する
   ![OrganizationのProjectsのTemplatesから新しくテンプレートを作成する](../image/image5-project-new-template.png)
- 既存のProjectをテンプレートに変換する
  - 既存のProjectのSettingsを開き、「Templates」で「Make template」を操作する
  ![ProjectのSettingsで、Templatesのメニューを確認する](../image/image5-template-menu-in-project-settings.png)
- 既存のProjectをコピーして、テンプレートを新しく作成する
  - Projectの三点リーダーのボタンから「Copy as template」を選択する
    ![Projectの三点リーダーのボタンから「Copy as template」を選択する](../image/image5-project-copy-as-template-quickly.png)
  - 前述のProjectのSettingsのTemplatesから操作する

## 返信テンプレート

返信テンプレートについて確認する。

- 任意の画面でアカウントアイコンをクリックし、`Settings`>`Code, planning, and automation`>`Saved replies`から返信テンプレートを作ってみる
  ![create saved replies](../image/image5-13.png)
- Issue/Pull requestに、saved repliesを使って返信してみる
  ![use saved replies](../image/image5-14.png)

---
[前ドメインへ](../domain4/README.md)  
[次のドメインへ](../domain6/README.md)  
[目次へ](../README.md)
