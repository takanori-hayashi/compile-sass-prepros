# 1. Propresのインストール
- https://prepros.io/downloads

osに応じてインストーラーをダウンロードしてインストール

# 2. ワークスペースをPropresに登録
1. githubから当リポジトリをダウンロード
2. 任意に作成したワークスペースの直下にsassディレクトリと、propres-6.configを配置
    - propres-6.configを使用することでプロジェクト毎に同じPropresの設定を適用します。設定内容は後術
3. propres-6.config最上部の `"name": "your project name",` を任意の名前に変更
4. Propresを起動し、ワークスペースのディレクトリをPropresにドラッグ&ドロップして登録

# 3. cssのアウトプット設定
PropresのGUIからcssファイルを出力するディレクトリを指定

1. projectsを選択し、settingをクリック
2. Compiler SettingsのSassの最下部RReplace Segments Withにcssを出力したいディレクトリを入力
    - プロジェクト毎に同じであれば固定してしまってもよい
    - 当リポジトリではdist/assets/cssとしています
    - 指定した最上層のディレクトリが存在してないと出力されないので注意