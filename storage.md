---
title: 倉庫
Sdescription: 倉庫
lang: ja_JP
---
<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-10FN64D8YF"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-10FN64D8YF');
</script>

# {{ page.title }}

[{{ site.title }}](./) > {{ page.title }}

特に必要では無くなったものの倉庫

## Oculus Touch インプットマッピング

[Oculus/OVRInput/Touchインプットマッピング](https://developer.oculus.com/documentation/unity/unity-ovrinput/?locale=ja_JP#touch-input-mapping)

![OculusTouchバーチャルマッピング](https://scontent-nrt1-1.xx.fbcdn.net/v/t39.2365-6/64515613_622041711631269_1500694343822868480_n.png?_nc_cat=103&ccb=2&_nc_sid=ad8a9d&_nc_ohc=w1QdasMFG5AAX-siIKU&_nc_ht=scontent-nrt1-1.xx&oh=44943d62637f66f1e02b986ec9656d70&oe=60281041)

## GitHub Pagesの設定

このサイトを作成したときのメモ

1. GitHub上でアカウントを作成
1. vrchatのリポジトリ(public)を作成
1. PC上でvrchatリポジトリのCloneを作成
1. SSH Keyの作成と登録(PC・GiHub)
1. PC上でgh-pagesブランチを作成
1. index.mdの作成
1. gh-pagesブランチのPush
1. GitHub上でgh-paseをGitHub PagesのSourceに選択しSave
1. `https://osaka99.github.io/vrchat/`へアクセスし、表示されることを確認

※初めてのことが多く、試しながらなので、実際はこの通りに進めていません。

その後の設定メモ

1. GitHub上でTheme Chooserを選択し、Pull(見た目対策+作成された_config.yml取得)
1. _config.ymlにSEQ対策など設定
1. Google Analyticsへの登録(アクセス解析用)
1. Google Search Consoleへの登録(SEO対策)
1. `site:osaka99.github.io/vrchat`で検索されることを確認

PlantUML対応メモ

1. VSCode+Markdown Preview EnhancedでインラインPlantUML検討
1. レンダリングできず断念
1. pumlファイルとして作成し、plantUMLサーバーへパスを渡しレンダリングする方式検討
1. 安全では無いページとなるため断念
1. VSCode+PlantUML(jebbs)でpumlファイルをsvg変換し、svgをリンク方式に決定

※plantUMLサーバーへ渡したときのパス。`http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.github.com/%アカウント?%/%リポジトリ?%/%ブランチ?%/%フォルダ%/test.puml`
