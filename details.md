# 1. Preprosのインストール
- https://prepros.io/downloads

osに応じてインストーラーをダウンロードしてインストール

# 2. ワークスペース作成
1. ローカルにワークスペース作成
2. githubから当リポジトリをダウンロード
3. 作成したワークスペースの直下にprepros-6.configを配置
    - prepros-6.configを使用することでプロジェクト毎に同じpreprosの設定を適用します。
    - prepros-6.configは設定ファイルなのでバージョン管理からは除外してください

# 3. Prepros設定
PreprosのGUIから設定を行う  
設定はproject > settingから行えます

## プロジェクト登録
Preprosを起動し、ワークスペースのディレクトリをPreprosにドラッグ&ドロップして登録  
有料ライセンスのポップアップが出ますが無視して無料使用できます。

## プロジェクト名変更（任意）
project > setting > General > Project Nameからプロジェクト名変更を行います。  
Prepros内での表示に関わる箇所なので任意で設定してください。

## cssの出力先指定
project > setting > Compiler SettingsのSassの最下部Replace Segments Withにcssを出力したいディレクトリを入力
- プロジェクト毎に同じであれば固定してしまってもよい

## cssのアウトプット設定について
### ベンダープレフィックス自動付与
autoprefixerの機能を使用してベンダープレフィックス自動付与します。  
そのためscssファイルにはベンダープレフィックスの記述は不要  
各ブラウザの2バージョン前までとIE11用のベンダープレフィックス自動付与します。

### cs minify
cssは圧縮して出力します。cssファイルの直接編集することは行わずscssファイルを編集してください。

# 4. コーディング
sassディレクトリ内にscssファイルを配置し、コーディングを行う。  
Preprosでファイルの更新を検知して自動でコンパイルが走ります。

- scss記法を使うので拡張子は.scssとしてください。
- cssの直接編集は行わず、変更する際はscssファイルを編集する
- sassの基本的な機能は下記urlを確認してください
    - https://gist.github.com/takanori-hayashi/9cd901edf7a840011ba9fb4c1c2d8c76

# その他
Preprosにはsassのコンパイル以外にも多くの機能がありますが、今回はsassのコンパイルのみに使用します。