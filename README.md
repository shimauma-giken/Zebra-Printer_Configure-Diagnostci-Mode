# Zebra-Printer_Configure Diagnostci Mode
プリンタ診断モードで受信データを取得する方法

1. プリンタにレシートを入れます。
   ※ラベルは望ましくない。

2. 下記のコマンドでプリンタを診断モードにします。
    ```java
    ! U1 setvar "device.diagnostic_print" "enabled"
    ```

3. プリンタにデータを配信します。

4. 配信したデータが全て印刷されるまで待ちます。

   <img width="50%" src="https://docs.zebra.com/content/dam/techpubs/media/printers/industrial/zt4x0/g-zt4x0-label-comm-dgnstc-test.svg/jcr:content/renditions/original">

5. 印刷データを確認します。

6. 診断モードを解除するにはプリンタを再起動してください。