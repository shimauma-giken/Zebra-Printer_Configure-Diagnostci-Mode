Zebra-Printer_Configure Diagnostic Mode
# プリンタ診断モードで受信データを取得する方法

<img width="50%" src="https://www.zebra.com/content/dam/zebra_dam/global/zcom-web-production/web-production-photography/hero-photos/printer-supplies-photography-web-desktop-printer-labels-16x9-3600.jpg.imgw.3600.3600.jpg">

想定した印刷ができないときに、まず切り分けるポイントはプリンタが受信しているデータです。  
</br>

|状況| 対策|
|-|-|
| プリンタが誤ったデータを受信している | 送信データ、アプリ、通信などを見直す |
| プリンタが適切なデータを受信している | プリンタの設定、プリンタの不具合などを見直す |

</br>

プリンタでどのようなデータを受信しているか確認することがファーストステップとなります。  
ゼブラプリンタには診断モードがあるため、受信データの内容を確認することが容易です。

</br>

特に下記のような状況が発生しているときに有用な確認方法です。
- 日本語を印刷したときに文字化けする。
- QRなどのバーコード情報が想定したものと異なる。

</br>
</br>

## プリンタの受信データを取得する方法

1. プリンタにレシートを入れます。
   ※ラベルは望ましくない。

2. 下記のコマンドでプリンタを診断モードにします。
    ```java
    ! U1 setvar "device.diagnostic_print" "enabled"
    ```

   ※ プリンタメニューで設定する場合の手順は、ユーザーズガイドを参照ください。
    

4. プリンタにデータを配信します。

5. 配信したデータが全て印刷されるまで待ちます。

   <img width="50%" src="https://docs.zebra.com/content/dam/techpubs/media/printers/industrial/zt4x0/g-zt4x0-label-comm-dgnstc-test.svg/jcr:content/renditions/original">

6. 印刷データを確認します。

7. 診断モードを解除するにはプリンタを再起動してください。

<br/><br/>

### 備考

下記の方法でも、診断モードにすることが可能です。運用上、こちらの方法が望ましい場合は、下記の手順で診断モードにしてください。

1. ~JDコマンドの実行
2. フィードボタンを押下しながら、電源ON
3. ファームウェアアップデート直後にプリンタに対してデータ入力・ボタン操作する
