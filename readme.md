# Azure Media Player CSS Custmize Test
Azure Media Player の動作やみかけを CSS でカスタマイズするテスト。

## How to Setup
- このリポジトリをフォーク
- Azure Static Web App (静的 Web アプリ) を新規作成
    - リソースグループ : 任意
    - 名前 : 任意
    - ホスティングプラン : Free
    - Azure Functions とステージングの詳細 : East Asia
    - ソース : GitHub
    - 組織 : GitHub の組織名
    - リポジトリ : このリポジトリをフォークしたリポジトリを選択
    - 分岐 : main
    - ビルドのプリセット : Custom
    - アプリの場所 : **/src**
    - API の場所 : 空欄
    - 出力先 : 空欄
- 「確認及び作成」でデプロイ
- GitHub Actions で自動的にデプロイされるのでしばし待機
- Azure Portal から作成した Static WebApp を開いて、基本 > URL にある URL を開く
- あとは、このリポジトリを VSCode 等で開いて HTML や CSS を変更してコミットするたびに自動で GitHub Action が走ってアップデートされます。便利！

## How to Customize
src ディレクトリ内には 3 つのファイルが入っています。
- index.html : Azure Media Player を組み込み済みの HTML ドキュメント
- amscustomize.css : Azure Media Player のみかけを CSS で変更する方法の例が含まれる CSS ファイル
- decoration.css : サイト全体の見かけをちょっとマシにするためのオマケ（このファイルは無視していいです）

### 例えば字幕領域の文字サイズを小さくしたい時は
以下のようなセレクターを書いてあげればよいです。

```css
/*字幕領域のフォントサイズを 15px に設定*/
.amp-default-skin .vjs-text-track-display>div>div {
  font-size: 15px !important;
}
```

他の要素についても、F12 ツールとかで要素ごとにセレクターを書いてあげればどうにかなると思います。

## Demo Sample
[こちら](https://brave-desert-0b0189a00.azurestaticapps.net)