# gitの操作に関する習得

## [gitの操作に関する習得(1)のリンク](https://redmine.syon.co.jp/issues/4081)
### 学習手順
- リポジトリ作成(githubのWeb上からご自身のアカウントに対し、新規リポジトリを作成します。名前は任意で大丈夫ですが、"GitLearning"とかでいいと思います)

* クライアントにてgit cloneコマンドを用いて、上記で作成したリポジトリを複製してください。(これを完了するまでの間に、クライアント側でgithubに接続するための初期設定など必要になるかと思います。)

+ gitについて把握した内容をテキスト形式(.txt)でローカル上のリポジトリ内に作成してください。

- 作成したファイルをgit add/git commitコマンドで反映してください。

- git pushコマンドでgithub上へpushしてください。

### 作業
#### 6/2(火)
##### デベロッパ・ツールインストール

  ターミナルで以下を実行したら、『"xcode-select"コマンドを実行するには、コマンドライン・デベロッパ・ツールが必要です。ツールを今すぐインストールしますか？』のダイアログが出たので、「インストール」を実行。

    $ git -v


　改めて、バージョンを確認するコマンドを打って、gitが動くことを確認

    $ git --version

    git version 2.24.3 (Apple Git-128)

#### 6/4(木)
- CreateRepository
  https://github.com/nkumiko93/GitLearning.git

- visual studio codeのインストールと設定

- git cloneでリポジトリを複製する

    $ git clone https://github.com/nkumiko93/GitLearning.git

    $ git push https://github.com/nkumiko93/GitLearning.git

### gitについて把握したこと
  ・ソース編集などをして、コミットしてもあくまでローカル環境のリポジトリのみの変更なので、
    必ず、リモートリポジトリへの反映が必要になること。

## [gitの操作に関する習得(2)のリンク](https://redmine.syon.co.jp/issues/4087)
### 学習手順
　〜 省略 〜

### git pullコマンド・git branchコマンドについて理解したこと
#### git pull
リモートリポジトリの内容をローカルリポジトリ内にマージする。

#### git branch
branchは、メインのプロジェクト以外に、並行して動く別プロジェクトがあった場合など、一時的に別に枝分かれしたリポジトリを作成して、プロジェクト終了後にメインにマージさせたりするために使う。
ローカル環境でもbranchを分けることも可能だが、管理をしっかりする必要があると感じた。
