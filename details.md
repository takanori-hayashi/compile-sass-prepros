# 1. Preprosのインストール
- https://prepros.io/downloads

osに応じてインストーラーをダウンロードしてインストール

# 2. ワークスペースをPreprosに登録
1. githubから当リポジトリをダウンロード
2. 任意に作成したワークスペースの直下にsassディレクトリと、prepros-6.configを配置
    - prepros-6.configを使用することでプロジェクト毎に同じpreprosの設定を適用します。設定内容は後術
    - prepros-6.configは設定ファイルなのでバージョン管理からは除外してください
3. prepros-6.config最上部の `"name": "your project name",` を任意の名前に変更
4. Preprosを起動し、ワークスペースのディレクトリをPreprosにドラッグ&ドロップして登録
    - 有料ライセンスのポップアップが出ますが無視して無料使用できます。

# 3. cssのアウトプット設定
PreprosのGUIからcssファイルを出力するディレクトリを指定

1. projectsを選択し、settingをクリック
2. Compiler SettingsのSassの最下部Replace Segments Withにcssを出力したいディレクトリを入力
    - プロジェクト毎に同じであれば固定してしまってもよい
    - 当リポジトリでは例としてdist/assets/cssとしています
    - 指定した最上層のディレクトリが存在してないと出力されないので注意
3. sassディレクトリ内にscssファイルを配置
    - Preprosがscssファイルを監視しているので自動でコンパイルが走ります
    - scss記法を使用するので、拡張子は.scssとしてください

## cssのアウトプット設定
### ベンダープレフィックス自動付与
autoprefixerの機能を使用してベンダープレフィックス自動付与します。
そのためscssファイルにはベンダープレフィックスの記述は不要
各ブラウザの2バージョン前までとIE11用のベンダープレフィックス自動付与します。

### cs minify
cssは圧縮して出力します。cssファイルの直接編集することは行わずscssファイルを編集してください。

# その他
Preprosにはsassのコンパイル以外にも多くの機能がありますが、今回はsassのコンパイルのみに使用します。