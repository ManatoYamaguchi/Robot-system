## デバイスドライバの作成
---

## 実装内容

ロボットシステム学第7,8回の講義内で作成したデバイスドライバに変更を加え作成しています。
* 0を入力すると赤色LED,緑色LEDの両方とも消灯する。
* 1を入力すると赤色LEDは消灯し,緑色LEDは点灯する。
* 2を入力すると赤色LEDは点灯し,緑色LEDは消灯する。
* 3を入力すると赤色LED,緑色LEDの両方とも点灯する。

---

## 使用するもの

* Raspberry Pi 4
* ブレッドボード
* LED *2
* 抵抗(300Ω) *2
* ジャンパー線　オスーメス *3

---

## 回路

<img src=https://user-images.githubusercontent.com/72900954/101147435-b7e58f00-365f-11eb-8fc7-64f409f82b8b.jpeg>
LEDのアノードがそれぞれGPIO24,GPIO25に接続されています。

---

## ビルド

* $ git clone https://github.com/ManatoYamaguchi/Robot-system.git 
* $ cd Robot-system/myled
* $ make
* $ sudo insmod myled.ko
* $ sudo chmod 666 /dev/myled0

---

## 実行する場合

* 0を入力する場合　
      $ echo 0 > /dev/myled0
  
  赤色LED,緑色LEDの両方とも消灯します。
  
* 1を入力する場合　
      $ echo 1 > /dev/myled0
      
  赤色LEDは消灯し,緑色LEDは点灯します。
  
* 2を入力する場合　
      $ echo 2 > /dev/myled0
      
  赤色LEDは点灯し,緑色LEDは消灯します。
  
* 3を入力する場合　
      $ echo 3 > /dev/myled0
      
  赤色LED,緑色LEDの両方とも点灯します。
 
---

## 実行動画

動画URL : https://youtu.be/qCr7hVg5pgQ

---

## ライセンス

