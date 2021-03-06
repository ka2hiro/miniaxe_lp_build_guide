# MiniAxe LP 組立説明書

_The English version of the build guide is [here](README_en.md)._

## 組み立ての前に
* はんだごてや工具、部品等でのケガに注意してください。
* 作業中に席を離れるときは、はんだごての電源を確認してください。
* 非常に小さい部品が含まれていますので、失くさないように注意してください。

### Rev 1.0 での制限事項について
PCB の rev 1.0 では、Kailh ロープロファイルスイッチのクリッキータイプ（白軸）を正式にサポートしていません。クリッキータイプ（白軸）にのみ存在するピンを受ける穴が基板上に設けられていないためです。新たにスイッチを選択、購入する際はご注意ください。

なお、既にクリッキータイプ（白軸）をお持ちで、PCBと干渉せずに取り付けられる場合は、そのままお使いいただくこともできますが、正式にサポートされている構成ではありませんので、ご留意ください。

## 内容物の確認
キットには以下の部品が含まれています。作業前に不足がないか確認してください。

はんだ済みキットには、下記番号の(13)以降の部品のみ同梱されていますので、ご確認ください。



![キットの内容物](images/IMG_3092.jpg)

番号 | 名前      | 値     | 個数 | 備考                | 部品番号
:----|:--------|:-----|:----|:-----------------|:-------
1  | PCB      |       | 2    | 左右1枚ずつ         |
2  | 抵抗      | 10kΩ  | 5    | 予備1、緑シールまたはマーカ<sup>[1](#marker)</sup>、部品本体に"103"という表記あり | R1, R4
3  | 抵抗      | 22Ω   | 5    | 予備1、黄シールまたはマーカ<sup>[1](#marker)</sup>、部品本体に"220"という表記あり | R2, R3
4  | コンデンサ | 1μF | 5   | 予備1、青シールまたはマーカ<sup>[1](#marker)</sup>、色が濃い | C1, C3
5  | コンデンサ | 0.1μF | 3 | 予備1、シールなし    | C2
6  | コンデンサ | 22pF  | 5 | 予備1、赤シールまたはマーカ<sup>[1](#marker)</sup>、色が薄い | C4, C5
7  | ショットキーダイオード |       | 2 |                  | D1
8  | 水晶発振子 | 16MHz | 2 |                  | Y1
9  | MPU      | ATMEGA32U4-AU | 2 |              | U1
10  | USBコネクタ | Micro Bメス | 4 |           | J1, J2
11 | タクトスイッチ |    | 2 |                  | SW20
12 | スイッチソケット |  | 36 |                 | SW1 - SW18
13 | M2ネジ    | 3mm | 16 |                    |
14 | M2金属スペーサ | 3.5mm | 8 |               |
15 | トッププレート |     | 2 |                 |
16 | ボトムプレート |     | 2 |                 |
17 | ゴム足       |      | 10 |                |
18 | USBケーブル  |       | 1 | キーボード間接続用 |

## その他に必要なもの
キットを完成させるためには、以下の部品を別途用意する必要があります。

* キースイッチ（ Kailh ロープロファイルタイプ（赤軸、茶軸）のみサポート。**白軸はサポートしていません** ）
* キーキャップ（ Kailh ロープロファイルタイプ ）
* USB Micro B ケーブル（PCとの接続用）

## 作業に必要な工具
組立作業には、最低限以下の工具が必要となります。

* はんだごて（温度調節できるものが望ましい）
* はんだ
* ピンセット
* プラス(+)ドライバ
* ルーペ
* フラックス

その他、必要に応じて以下も用意すると良いです。

* フラックス洗浄剤
* はんだ吸取線
* テスタ



# 組立手順

はんだ済みキットでは、「[USBデバイスとして認識されることを確認する](#usbデバイスとして認識されることを確認する)」の項目から組立を進めてください。



## MPUをつける
1. MPU上に付いている●印と、基板上の○印を合わせて配置します。
2. 4方向全てのピンがパッド上に乗っていることを確認し、はんだ付けします。

![MPU](images/IMG_3131.jpg)

QFPパッケージのはんだ付けは、この[動画](https://www.youtube.com/watch?v=-8SRkSjkZ8A)が参考になるかもしれません。

## 水晶発振子をつける
1. 水晶発振子の長辺（どちらの長辺でも構いません）が、基板上の部品番号(Y1)の位置に来るように向きを合わせ、4つのパッドの中心に配置します。
2. 水晶発振子の角に少しだけ端子部分が見えるので、そこをこて先で温めつつはんだを流し込みます。

![Crystal](images/IMG_3134.jpg)

SMDタイプの水晶発振子のはんだ付けは、この[動画](https://www.youtube.com/watch?v=14fJTgFg03M)が参考になるかもしれません。

## 抵抗をつける
1. 抵抗 R1 〜 R4 を取り付けます。部品が本当に小さいのであっという間に見失ってしまいますので、注意してください。作業するときは一度に一つずつ、テープから取り出してください。

![Registor](images/IMG_3135.jpg)

## コンデンサをつける
1. コンデンサ C1 〜 C5 を取り付けます。部品自体に数値や文字が書かれていないので、値の異なるものを混在させると見た目では識別できなくなります。作業するときは一度に一つずつ、テープから取り出してください。

![Capacitor](images/IMG_3136.jpg)

## ショットキーダイオードをつける
1. ダイオード D1 には取り付ける向きがあります。パッケージの片方が白く帯状に塗られている部分を、基板上のダイオードの記号の縦棒の位置に合わせてください。

![Diode](images/IMG_3133.jpg)
![Diode](images/IMG_3137.jpg)

## USBコネクタをつける
1. 外側のスルーホール部分ではなく、先に端子部分からはんだ付けするとズレることなく取り付けできます。

![USBConnector](images/IMG_3139.jpg)

## タクトスイッチをつける
1. タクトスイッチは、4本の端子以外にも側面に端子があり、少しだけ金属の部分が見えていますので、その部分にはんだごてを当てて、ハンダを流し込むようにします。

![TactSwitch](images/IMG_3140.jpg)

## ソケットをつける
1. _ソケットを取り付ける向きが、他と異なる場所が中央付近に２か所(SW7, SW8)あるので注意してください。_
2. 間違った向きに取り付けると、キースイッチを取り付ける真ん中の穴がふさがれてしまいます。
3. まず、全てのソケットの片側だけをはんだ付けしてから、向きを間違えてないか確認し、それから残りの部分をつけると失敗しにくいです。

![Socket](images/IMG_3142.jpg)

## 正しくはんだ付けされているか確認する
回路図( [左側](files/MiniAxeLeft.pdf) 、[右側](files/MiniAxeRight.pdf))を参考に、正しくはんだ付けされているか確認します。

コンピュータに接続する前に、少なくとも以下の項目は確認しましょう。

1. UVCC-GND間、VCCーGND間がショートしていないことを確認します。
2. MPUのピンがブリッジしていないことを確認します。
4. USBコネクタの端子がブリッジしていないこと確認します。


## USBデバイスとして認識されることを確認する
キーボードをコンピュータにつないで、USBデバイスとして認識されることを確認します。

* Macの場合は、「システム情報」を起動して、「ATm32U4DFU」というデバイスが見えているか確認します。
![システム情報](images/system-info.png)

* Windowsの場合は、「デバイスマネージャ」を起動して、「ATm32U4DFU」というデバイスが見えているか確認します。
![デバイスマネージャ](images/device-manager.png)

* はんだ済みキットでは、MacまたはWindowsで「MiniAxe」が見えているか確認します。

USBデバイスとして認識されない場合は、全ての部品が正しくはんだ付けされているか、回路図を参考に再度確認してください。

## トッププレートをつける
1. M2x3mmネジをトッププレートにはめ込み、マスキングテープ等でネジの頭を固定します。
![トッププレート](images/IMG_3149.jpg)
2. トッププレートを裏返し、金属スペーサをつけます。
![樹脂スペーサ](images/IMG_3151.jpg)
3. 基板と組み合わせます。
![金属スペーサ](images/IMG_3153.jpg)

## ボトムプレートをつける
1. M3x3mmネジをボトムプレートにはめ込み、基板上の金属スペーサに対して、少しずつ、対角線上のネジを選んで（左上→右下→右上→左下などの順序で）、均等に締め付けていきます。_1本ずつきっちり締め付けていくと、最後のネジが噛み合わなくなることがあるので、注意してください。_

![ボトムプレート](images/IMG_3156.jpg)

## ゴム足をつける
1. ゴム足をボトムプレートにつけます。
![ゴム足](images/IMG_3158.jpg)

## キースイッチとキーキャップ をつける
1. お好みのキースイッチとキーキャップ を取り付けます。 (_Kailhロープロファイルスイッチのみサポートしています。Cherry MX互換タイプはサポートしていませんので、注意してください。_)
2. _キースイッチのピンは曲がりやすいので、まっすぐになっていることを確認してから取り付けてください。また、 SW7とSW8は向きが他とは反対になっているので、注意してください。_

## ファームウェアを書き込む
__はんだ済みキットでは、デフォルトキーマップが既に書き込まれています。__

ファームウェアはQMKを利用します。以下のリポジトリをクローンしてください。

[qmk_firmware](https://github.com/qmk/qmk_firmware)

クローンしたら、ローカルリポジトリのディレクトリへ移動し、以下のコマンドを実行すると、ファームウェアを書き込むために待機状態になりますので、キーボードを接続してください。すでにキーボードが接続されている場合は、そのまま書き込みが始まります。

~~~
$ make miniaxe:default:dfu
~~~

初めてファームウェアを書き込む場合は、リセットスイッチを押す必要はありません。

ファームウェアをビルドする環境の構築は、[こちらのドキュメント](https://docs.qmk.fm/#/getting_started_build_tools)を参考にしてください。

## 完成！
これで完成です。おつかれさまでした。
![Done](images/IMG_3159.jpg)

---

<a name="marker">1</a>: キットによってはマーカで色をつけたものもあります。  

