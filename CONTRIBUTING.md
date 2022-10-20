## 環境構築
- 以下は VSCode + remote container を使った方法
  - Ctrl-P → `>` を入力 → `Dev Containers: Open Folder in Container...` でこのリポジトリを選択
  - ひたすら待つ
    - postCreateCommand で `bundle install` まで自動でやってくれます
    - 画面下のターミナルに `Done. Press any key to close the terminal.` が表示されたら完了です

## 動作確認
- Ctrl-P → `>` を入力 → `Tasks: Run Test Task` を選択
- 画面右下に `ポート 4000 で実行されているアプリケーションは使用可能です。` というダイアログが出るので、ダイアログ中の `ブラウザで開く` をクリックすればブラウザ上で確認できます。
  - `エディターでのプレビュー` をクリックすればエディタ内で確認できます。
  - ブラウザから http://localhost:4000/ を直接開いて確認することもできます。

## `Gemfile` を更新した場合
ターミナルから `bundle update` を実行し、`Gemfile.lock` および各 gem を更新する必要があります。

