---
title: VRChatをOculus Quest2で楽しむには
description: VRChatをOculus Quest2単体やOculus LinkでPC接続して楽しむための情報を載せています。
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

VRChatをOculus Quest2で楽しむための情報がうまく探せなかったり、記事が古かったりしたため、ポイントを絞ってまとめました。(最終更新日:2021/01/18)

- [公式](#公式)
- [遊び方(作成未定)](#遊び方)
- [環境・操作](#環境操作)
  - [Oculus Quest2の各部名称](#oculus-quest2の各部名称)
  - [Oculus Quest2の操作](#oculus-quest2の操作)
  - [VRChatのアバター利用制限・見え方](#vrchatのアバター利用制限見え方)
  - [VRChatのアバターをQuest対応にする](#vrchatのアバターをquest対応にする)
  - [VRChat Oculus Quest2のハンドサイン](#vrchat-oculus-quest2のハンドサイン)
  - [Oculus Quest2+Oculus LinkでVRChatにPC接続しマイクが認識されない](#oculus-quest2oculus-linkでvrchatにpc接続しマイクが認識されない)
  - [左右にAction Menuを出す](#左右にaction-menuを出す)
- [倉庫](#倉庫)

## 公式

- [VRChat(英語)](https://hello.vrchat.com/)
- [Oculus(日本語)](https://www.oculus.com/)
- [Oculusサポートページ(日本語)](https://support.oculus.com/)

## 遊び方

作成未定

## 環境・操作

### Oculus Quest2の各部名称

|No|内容|
|--|--|
|1|頭にかぶるものはOculus Quest2 ヘッドセット|
|2|ヘッドセットの右側にあるボタンが電源ボタン|
|3|ヘッドセットの下側にあるボタンが音量ボタン|
|4|ヘッドセットの左側にある差し込み口がOculus Linkとイヤホンの差し込み口|
|5|コントローラーの名称はOculus Touch|
|6|右コントローラーにはAボタン、Bボタン、Oculusボタン(⊂⊃ボタン)、サムスティック(上から押し込んでボタンにもなる)、サムレスト(ABボタンの左側)、トリガーボタン、グリップボタン|
|7|左コントローラーにはXボタン、Yボタン、Menuボタン(三ボタン)、サムスティック(上から押し込んでボタンにもなる)、サムレスト(YXボタンの右側)、トリガーボタン、グリップボタン|

### Oculus Quest2の操作

|判定|内容|
|--|--|
|Press判定|A、B、X、Yボタン、Oculusボタン、Menuボタン、左右コントローラーのサムスティックボタン、トリガーボタン、グリップボタン|
|接触判定|A、B、X、Yボタン、左右コントローラーのサムスティック、トリガーボタン、グリップボタン<br>※指などでかるく触れれば判定されます。|
|長押し判定|Oculusボタン、Menuボタン|
|その他|ヘッドセットやコントローラーの向き変更、移動|

### VRChatのアバター利用制限・見え方

|PC|Quest|Type|内容|
|--|--|--|--|
|〇|×|PC専用|PC接続のみで利用できるアバター|
|〇|〇|PC+Quest|PC接続、Quest単体の両方で利用できるアバター|
|×|〇|Quest専用|通常存在しないアバター|

![avatar](assets/avatar.svg)

### VRChatのアバターをQuest対応にする

|No|内容|
|--|--|
|0|前提：既にPC対応のアバターをVRChatにアップロードできていること。<br>※SDK3.0しか確認していません。<br>※Quest対応のアバターを追加することで、PC+Questのアバターにすることができます。|
|1|PC対応のファイルを退避する(Gitなどで別途Quest用のブランチを切るのが良いと思う)|
|2|Hierarchyの要素を順に選択し、Shaderを「VRChat/Mobile/Toon Lit」に変更する。|
|3|Hierarchyの検索欄に「script」と打ち込み検索する。|
|4|検索結果を順に選択し、Inspectorで「Dynamic Bone(Script)」とあれば右側の設定アイコンをクリックし、「Remove Component」を選択して削除する。|
|5|Unityの「File/Build Settings」からPlatform欄の「Android」を選択し、「Switch Platform」ボタンを押す。|
|6|InspectorのPipeline ManagerでBlueprint IDにPC対応アバターのIDを設定する(PC対応アバターをアップロードすると、IDが自動で設定されるため、続けて作業した場合、この作業は不要なはず)|
|7|PC対応アバターのときと同様の操作でVRChatにアップロードする。|

### VRChat Oculus Quest2のハンドサイン

ほとんどのアバターにはハンドサインによる表情等の変化に対応しており、覚えておいて損はない操作になるはずです(割り当てはアバター側の設定)

|Sign|内容|
|--|--|
|Default|トリガーボタンPress|
|Fist|A、B、X、Yボタン、サムスティックのいずれか接触+トリガーボタンPress+グリップボタンPress|
|HandOpen|何も接触・Pressなし|
|FingerPoint|A、B、X、Yボタン、サムスティックのいずれか接触+グリップボタンPress|
|Victory|A、B、X、Yボタン、左右サムスティックのいずれか接触|
|Rock'n Roll|A、B、X、Yボタン、左右サムスティックのいずれか接触+トリガーボタンPress|
|Handgun|グリップボタンPress|
|Thumbs-Up|トリガーボタンPress+グリップボタンPress|

### Oculus Quest2+Oculus LinkでVRChatにPC接続しマイクが認識されない

既知の不具合らしく、下記のような手順を取る必要があります。

|No|内容|
|--|--|
|1|Oculus Quest2を起動してOculus Linkを挿し、データへのアクセスを許可してPCと接続する。|
|2|Oculus Quest2のメニュー/設定から「Oculus Link」を選択してRiftにする。|
|3|VRChatを起動してログインし、Settingを開いて、しゃべってみてMicrophoneの「Headsdet Microphone(Oculus Virtual Audio Device)」が反応するか確認する。|
|4|反応しなかったら、Oculusボタンを押し、Riftのメニューから「Oculus Linkをオフにする」を選択してオフにし、データのアクセスを許可を求められれば許可する。|
|5|Oculus Quest2のメニュー/設定から「Oculus Link」を選択して再度Riftにする。|
|6|VRChat画面に戻る(私の環境ではこの時地面に潜っていることがあり、その場合はVRChatを再起動する。私の場合はOculusボタンを押し、Riftのメニューから「ホーム」を選択してVRChatを閉じています)|
|7|再びVRChatにログインしてSettingを開き、しゃべってみてMicrophoneの「Headsdet Microphone(Oculus Virtual Audio Device)」反応するか確認する。|

※Oculus Linkを接続した状態で、PC側のサウンドコントロールパネル/録音で「既定のデバイス」が「Headset Microphone(Oculus Virtual Audio Device)」になっていなければ設定してください（既に設定されている場合、一旦別デバイスに変更し、戻すとうまくいくかもしれません）

※PC側のOculusアプリでデバイス設定/Quest2とTouchを選択し、「Quest2マイク」、「Quest2ヘッドホン」を選択することが公式おすすめのようです。その下にある「デバイスを設定」ですが一度は行っておくべきかもしれません。

※[Oculus QuestとOculus Linkのトラブルシューティング](https://support.oculus.com/358707732169608/)

### 左右にAction Menuを出す

左右合わせて２つのAction Menuを同時に出すための手順となります。

|No|内容|
|--|--|
|1|右側を普通に出す(B、Yボタンの通常メニューからEmote->Action Menu)|
|2|左コントローラーのMenuボタンを長押しAction Menuを出す。|

※音無テム(VRChatアバター)で、片方はフキダシテキスト選択、もう片方はフキダシ表示をするときに必要

## 倉庫

[倉庫](storage)

※特に必要では無くなったものの倉庫
