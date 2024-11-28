# Aximmetry

## 概要
VirtualProductionを手軽に行えるシステムを探していたところ、
- [Aximmetry](https://aximmetry.com/)

を見つけた。

やりたいことは、バーチャルスタジオにリアルタイムでグリーンバック撮影したものを合成すること。なるべく無償で行いたい。

- [Virtual Production demo with Aximmetry Eye mobile app--- Aximmetry](https://www.youtube.com/watch?v=dugtm2TlY44)

を見ると非常に簡単にできそうであるが、様々なところでハマったため、備忘録としてやり方を残す。

---
---
---

## 実施したいこと
1. UnrealEngineでバーチャルスタジオ制作
2. Aximmetry Eyeでグリーンバック撮影・Aximmetryで合成

---
---
---

## 準備
### Aximmetry
- Windows版のみ
- [SE/DE版](https://aximmetry.com/ja/aximmetry-de-se)があるが、UnrealEngineを利用する場合はDE版が必要
- [Aximmetryソフトウェア版](https://aximmetry.com/ja/products) Community Edition(廃止？)/Studio Edition(無料)/Professional Edition/Broadcast Editionがある
- [推奨動作環境](https://aximmetry.com/ja/hardware-configuration)はスペック高め
- ログインしてDownloadを見ると以下がある。
    - Aximmetry Studio DE 2024.3.0(必須)
    - Aximmetry用Unreal Engine 2024.3.0(必須)
    - Aximmetry.Common_Library_2024.3.0 パッケージ(必須)
    - Aximmetry.Studio_Demo_Sets_2024.3.0 パッケージ
    - Aximmetry.Tutorials_and_Samples_2024.3.0 パッケージ
> 通常、このファイルはAximmetryのインストール中に自動的にダウンロードされ、インストールされます。ドライブにバックアップしたい場合、または自動ダウンロードに問題がある場合のみ、こちらからダウンロードしてください。

と書いてあるが、自分でインストールの必要性があった。

### Aximmetry Eye
- [Aximmetry Eye](https://aximmetry.com/ja/aximmetry-eye)

調べた当初はオフィシャルページにTestFlight経由での案内が出ていた。
実際にTestFlightで起動を試すとベータテスト終了となっていた。
ところが、オフィシャルページの更新の前にAppStoreでリリースされていた。

現在はiPhone版のみでAndroid版は現在開発途中の模様。

### Windows-iPhone連携
#### 無線LAN接続
- 利用している無線LANがポート閉じていたり等様々な制約があったため、テザリングしたiPhoneにぶら下げることで接続することができた。
- 無線LANをインターネット接続しないでその下にぶら下げることも試したが、Aximmetry Eyeが起動時にインターネット接続を求めるため、この方法は不可。
- 無線LANの種類によると思われるが、接続エラーだったり、レイテンシーが遅かったり色々と問題があった。

#### 有線LAN接続
- iPhone14まではLightning端子。Lightning-Ethernetアダプタを使うことで有線LAN接続が可能となる。
- レイテンシー・バンド帯域的にも無線LANと比べると有利？？？？

