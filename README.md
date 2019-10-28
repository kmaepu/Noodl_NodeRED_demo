# Noodl_NodeRED_demo
　NoodlとNode-REDを連携し、気象情報を表示するUIのサンプルです。  
   
 Node-REDで[OpenWetherMAP](https://openweathermap.org/)から気象データを取得し、Noodlで作成したUIに表示します。  
 構成は次のようになっています。  
 
   ![構成図](https://github.com/kmaepu/Noodl_NodeRED_demo/blob/master/image/構成図.png)
   
   
Node-REDについては [こちら](https://nodered.jp/)を参照。  
Noodlについては[こちら](https://tensorx.co.jp/noodl-jp/)を参照。  

# 開発環境
　・Noodl　ver1.3.1 or ver1.4.0  
　・Node-RED ver0.20.7  
　・OpenWeatherAPI
 
# 使い方
1. このリポジトリをclone or ダウンロードでサンプルコードを入手  
2. 入手したフォルダ内のNode-REDフォルダにある「flows_sample.json」を、Node-REDの読み込みからインポート  
　次のように「クリップボードから読み込み」を開き、読み込むファイルをflows_sample.jsonにします。
 
 ![Node-RED フロー読み込み](https://github.com/kmaepu/Noodl_NodeRED_demo/blob/master/image/Node-REDフロー読み込み.JPG)

3. Noodlを起動し、入手したフォルダのNoodlフォルダにある「Wether_demo」をインポート  
  　ver1.3.1の場合、アカウント認証後画面の「Add external project」からインポートします。  
  　ver1.4.0の場合、アカウント認証後画面の「CREATE NEW PROJECT」-> 「Add external project」からインポートします。  
      
    ver1.3.1ではアカウント認証後に次のような画面が開きます。  
    ![Noodl プロジェクトインポート](https://github.com/kmaepu/Noodl_NodeRED_demo/blob/master/image/Noodl_プロジェクトインポート.JPG)
4. 外部MQTTサーバを用意  
  　Node-REDのMQTT brokerノードやmosquitto、shiftr.ioなどのMQTT brokerを用意。  
5. Node-REDのサンプルフローにあるMQTT inノードとMQTT outノードのサーバ設定に、MQTT brokerのURL等を入力する  
6. Noodlの「Project settings」にあるMQTT External Brokerにチェックを入れ、Broker URLに使用するMQTT brokerのURLを入力する   

# ライセンス
 Free
