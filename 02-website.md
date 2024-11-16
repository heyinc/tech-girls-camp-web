# ウェブサイトを作って、公開してみる

## GitHubに登録してみる

1. [GitHubの公式サイト](https://github.com/)にアクセスします。
2. 右上の「Sign up」ボタンをクリックします。
3. 必要な情報を入力してアカウントを作成します。

## GitHubにソースコードをプッシュしてみる

1. ローカルで作成したウェブサイトのファイルを、Gitで管理します。
   - コマンドラインで以下のコマンドを実行します。

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. GitHubで新しいリポジトリを作成します。
   - GitHub上で「New」ボタンをクリックし、リポジトリ名を入力して作成します。

3. リモートリポジトリにプッシュします。

   ```bash
   git remote add origin https://github.com/ユーザー名/リポジトリ名.git
   git branch -M main
   git push -u origin main
   ```

## GitHub Pagesでウェブサイトを公開してみる

1. GitHubのリポジトリページで、「Settings」タブをクリックします。
2. 左側のメニューから「Pages」を選択します。
3. 「Branch」の欄で「main」を選択し、「/ (root)」を指定します。
4. 「Save」をクリックすると、ウェブサイトが公開されます。
5. 公開URLが表示されるので、アクセスして確認してみましょう。
