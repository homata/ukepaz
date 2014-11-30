開発メモ
======

### 参考
* [Cordovaを用いた開発環境を構築する](http://www.buildinsider.net/mobile/bookhtml5hybrid/0401)



ログ
---------
プロジェクトを作成する
$ cordova create ukepaz jp.openfab.ukepaz  UkePaz -d
	- ディレクトリ: ukepaz
 	- アプリの識別:  jp.openfab.ukepaz
	- アプリプロジェクト: UkePaz
	- -dオプション、cordovaコマンド実行中の途中経過を表示

プロジェクトにAndroidとiOS用のファイルを追加
$ cd ukepaz
$ cordova platform add ios
$ cordova platform add android
$ cordova platform ls
	Installed platforms: android 3.6.4, ios 3.7.0
	Available platforms: amazon-fireos, blackberry10, browser, firefoxos

	プラットフォームから外す
	$ cordova platform remove ios

Androidエミュレータを利用する
$ cordova emulate android -d

iOSシミュレータを利用する (ver3.0以上)
$ npm install -g ios-sim
	-> https://github.com/phonegap/ios-sim.git
	$ brew install ios-sim (バージョンが古い？)
$ cordova emulate ios -d


Android実機
$ cordova run android
	- $ cordova run android -d  (デバッグモード)
	- wwwディレクトリ以下のファイルから、あるプラットフォーム用のプロジェクトを作成する
	- 作成したプラットフォーム特有のプロジェクトをビルドする
	- ビルドしたアプリを端末やエミュレータにインストールして実行する

アプリをホストするローカルなWebサーバを起ち上げることができます。
$ cordova serve android

cordovaコマンドの管理
$ npm update cordova -g
$ npm install cordova@3.0.0 -g

ionic
$ npm install -g cordova ionic

例）
* [Installing Ionic and its Dependencies](http://ionicframework.com/docs/guide/installation.html)
* [キミはionicを知っているか？AngularJS+PhoneGap+美麗コンポーネント群！](http://html5experts.jp/canidoweb/7359/)
$ ionic start myApp blank
$ ionic start myApp tabs
$ ionic start myApp sidemenu
キミはionicを知っているか？AngularJS+PhoneGap+美麗コンポーネント群！$ ionic start myApp tabs
	* cd into your project: $ cd myApp
	* Setup this project to use Sass: ionic setup sass
	* Develop in the browser with live reload: ionic serve
	* Add a platform (ios or Android): ionic platform add ios [android]
	* Build your app: ionic build <PLATFORM>
	* Simulate your app: ionic emulate <PLATFORM>
	* Run your app on a device: ionic run <PLATFORM>
	* Package an app using Ionic package service: ionic package <MODE> <PLATFORM>
$ cd myApp
$ ionic platform add ios
$ ionic build ios
$ ionic emulate ios

### ukedon pazzle
$ ionic start ukedon sidemenu
$ ionic setup sass
$ ionic serve
