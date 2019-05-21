# Preprosのインストール
- https://prepros.io/downloads

osに応じてインストーラーをダウンロードしてインストール

# Preprosの設定

インストール後プロジェクトのデフォルト設定を行う。
基本的に全てのプロジェクトでデフォルト設定でコンパイルを行う。

## 設定内容

### Project Defaults
Prepros左上のハンバーガーメニュー内 `Project Defaults` をクリックしてプロジェクトデフォルト設定を行う

#### General

プロジェクト毎の設定ファイルを作成せず、プロジェクトデフォルト設定でコンパイルします。

- Export Config
  - チェックを外す
- その他は任意

#### File Watcher

ファイルの監視設定。
拡張子scssファイルのみの更新を監視し、自動コンパイルする設定にします。

- Enable File Watcher
  - チェックする
- Watched Extensions
  - scssのみを残して削除
- その他は任意

#### Compailer Settings

Sassのコンパイルのみに使用するので、Sass項目のみを設定します。

##### Sass

- Auto Compile
  チェックする
- Source Map
  - チェックを外す
- Process With
  - Node Sassを選択
- Output Style
   - Expandedを選択
- Autoprefixer
  - チェックを入れる
- Minify Css
  - チェックを入れる
- Output
  - Output Type
    - Relative to Sourceを選択
  - Relative
    - `../css` を入力


#### Other Settings

Autoprefixerのみ設定します。

- Autoprefixer
  - Browsers
    - `last 5 versions, ie >= 11` を入力

### 設定不要
下記機能は使用しないので設定不要

- Live Preview
- Browser Sync
- Live Reload
- FTP Setting