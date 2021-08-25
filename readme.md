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

## Demo Sample
[こちら](https://brave-desert-0b0189a00.azurestaticapps.net)