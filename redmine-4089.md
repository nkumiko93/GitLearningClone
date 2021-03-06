# WebアプリケーションとWebフレームワーク基礎

[チケット#4089のリンク](https://redmine.syon.co.jp/issues/4089)

## MVCアーキテクチャについて

### MVCアーキテクチャとは(概要)

**MVC**とはModel・View・Controllerの略で、**アーキテクチャ**は、思想や構造を指す。

MVCアーキテクチャがない時期は、ビジネスロジック部分と、デザイン部分(UIも含む)が混在していたが、  
ビジネスロジック部分と、デザイン部分を分けることで、それぞれの分野が得意な会社などに分業が可能となった。


### M,V,Cそれぞれが表すモノの役割
#### M：Model
Modelは、システムの中でビジネスロジック、データアクセスを指し、**システム本体**にあたる。  
具体的な機能として、アプリケーションデータや関数、データベースへのアクセス、データ管理などがある。

#### V：View
Viewは、レイアウトの部分を指す。  
UIを表示するためのコンポーネント(部品)であり、データ入力フォームやグラフといったデザインや**レイアウトに関わる部分**を担当しており、HTML生成を担っている。

#### C：Controller
Controllerは、**処理の制御**を行っている。  
具体的には、ModelとViewの仲介役であり、Viewから受け取ったデータをModelに渡し、Modelに処理されたデータをViewに渡す処理を行う。  
Controllerのクラス構造はURLに直結するため、Controllerクラスとそのメソッドの組み合わせでURLが形成される。
Controllerは、リクエスト情報を直接処理する。

## Webフレームワークについて

### Webフレームワークとは
フレームワークは、システム開発を効率化してくれる機能群。
機能群のみならず、ソフトウェアの骨組みまでを用意してくれているため、少ないコードで意図する機能やデザインが実現できる。

Webフレームワークは、Javascript、Ruby、PHP、PythonなどのWebアプリケーション開発言語用のフレームワークを指す。

### Webフレームワークをつかうことのメリットなど
機能群のみならず、ソフトウェアの骨組みまでを用意してくれているため、少ないコードで意図する機能やデザインが実現できる。

プログラミングコードは、100人プログラマーがいたら、100通りの書き方が生まれてしまうが、フレームワークで、
機能実現の文法をルール化することで誰が見ても分かりやすいプログラミングコードを実現でき、実装漏れ防止にもなる。

デメリットとしては、フレームワークのルールを覚える労力が必要がある。

### MVCアーキテクチャに基づいたWebフレームワークの例を列記(例：PHP+CakePHP、など)、また、その大まかな特徴

例：PHP + CakePHP、Java + Struts

#### PHP + CakePHP
Ruby on Railsというフレームワークが先行して流行していたが、この概念の多くを取り入れ、Rails流の高速開発とPHPの機動性を兼ね備えたフレームワークのcakePHPが作られた。

この「CakePHP」はウェブ開発を単純に簡単にできるように開発されており、高速に開発するための仕掛けが随所に盛り込まれている。

##### 統合された柔軟なO/Rマッピング（ActiveRecordパターン）

O/Rマッピング（PHP上のオブジェクトとデータベースを関連付けするための仕掛け）はSQL文を書くことなく非常に短い記述でレコードの抽出や書き換えが行えます。さらに関連付け（アソシエーション）を記述することで，関連したテーブルの情報を自動的に取得できます。

##### scaffolding機能

簡単なコントローラをひとつ用意するだけで、テーブルの一覧・追加・削除・編集(Create,Read,Update,Delete) の画面などを簡単に実装することができるといった機能を提供されております。デメリットはレイアウトなどのカスタマイズが難しい点があります。
主にカスタマイズが少ないマスタ画面などに用いることで工数削減が図れます。

##### bakeコマンドによるプログラム自動生成機能

bakeコマンドを実行すると対話的に次々と入力を求められ、それに答えていくことでMVCモデルに沿ってのモデル/ビュー/コントローラのPHPプログラムを自動生成する機能になります。
コマンドのパラメータによってテーブルの一覧・追加・削除・編集画面などのPHPプログラムが自動生成されるのです。
デメリットはテーブル変更時は個別対応が必要です。

#### Java +  Struts

Strutsは、Java開発では最も有名なフレームワークと言っても言い過ぎではない。

Strutsの特徴として、独自のカスタムタグの利用や、Actionクラスとstruts-config.xmlでの画面遷移の管理、バリデータ（入力チェック）機能の提供などが挙げられる。

Struts2ではアノテーションによる設定ファイルの削減や、DIコンテナ機能による外部ファイルでクラスの依存関係を設定できるなどの改良が加えられている。

フレームワークとしての歴史が古い分、Strutsを使用したシステムは多く存在するが、脆弱性の発見などによって別のフレームワークに移行するユーザーも増えている。Strutsでシステム構築するにあたっては、脆弱性を把握したうえで構築する必要がある。

#### Java + SAStruts

沖縄出身の比嘉康雄さんを中心とするメンバーによるもの。  
SeaserプロジェクトがStrutsをベースとして開発されたフレームワーク。  
Seasarプロジェクトが提供するプロダクトの多くは 2016年9月26日 をもって EOL (End of Life) となった。
