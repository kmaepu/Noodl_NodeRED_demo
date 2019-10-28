# Noodl_NodeRED_demo
　NoodlとNode-REDを連携し、気象情報を表示するUIのサンプルです。  
   
 Node-REDで[OpenWetherMAP](https://openweathermap.org/)から気象データを取得し、Noodlで作成したUIに表示します。  
   
   ![構成図](https://github.com/kmaepu/Noodl_NodeRED_demo/blob/master/構成図.png)
   
   
Node-REDについては [こちら](https://nodered.jp/)を参照。  
Noodlについては[こちら](https://tensorx.co.jp/noodl-jp/)を参照。  

# 開発環境
　・Noodl　ver1.3.1 or ver1.4.0  
　・Node-RED ver0.20.7  
　・OpenWeatherAPI
 
# 使い方
1. このリポジトリをclone or ダウンロードでサンプルコードを入手  
2. 入手したフォルダ内のNode-REDフォルダにある「flows_sample.json」を、Node-REDのフローの読み込みからインポート  
3. Noodlを起動し、入手したフォルダのNoodlフォルダにある「Wether_demo」をインポート  
  　ver1.3.1の場合、アカウント認証後画面の「Add external project」からインポートします。  
  　ver1.4.0の場合、アカウント認証後画面の「CREATE NEW PROJECT」-> 「Add external project」からインポートします。  
4. 外部MQTTサーバを用意  
  　Node-REDのMQTT brokerノードやmosquitto、shiftr.ioなどのMQTT brokerを用意。  
5. Node-REDのサンプルフローにあるMQTT inノードとMQTT outノードのサーバ設定に、MQTT brokerのURL等を入力する  
6. Noodlの「Project settings」にあるMQTT External Brokerにチェックを入れ、Broker URLに使用するMQTT brokerのURLを入力する   

# ライセンス
 Free
