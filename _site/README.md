# RFC-HP-72
#### 会社ホームページ：masterにマージ→自動公開

#### 必須環境
* [Ruby](https://www.ruby-lang.org/ja/) ([RubyInstaller for Windows](https://rubyinstaller.org/downloads/))
* [rails](https://rubyonrails.org/)
* [jekyll](http://jekyllrb-ja.github.io/)


#### 環境構築

##### STEP1:Ruby(with DEVKIT)のインストール
  1. [RubyInstaller for Windows](https://rubyinstaller.org/downloads/)からRuby+Devkit 2.6.5-1 (x64)をインストール
  1. RubyInstaller-devkitを起動する  (初回はMSYS2の項目にチェックを入れる)
  ![msys2](https://user-images.githubusercontent.com/50974298/74997747-40f95400-549a-11ea-9f6d-17fc7b959c4d.png)
  1. RubyInstaller2 for Windows起動後 3 番を実行  (3 - MSYS2 and MINGW develop toolchain)
  ![rbinst](https://user-images.githubusercontent.com/50974298/74997758-46ef3500-549a-11ea-803f-75152ea40512.png)
  1. `$ ruby -v`  
  でrubyのバージョンが表示されれば完了  
  ![rbv](https://user-images.githubusercontent.com/50974298/74997763-48206200-549a-11ea-9404-ab7fa544dcd5.png)

##### STEP2:Rails/jekyllのインストール  
  ##### 【rails】
  1. `$ gem install rails`
  1. `$ rails -v`  
  でrailsのバージョンが表示されれば完了
  ##### 【jekyll】
  1. `$ gem install bundler jekyll`
  1. `$ jekyll -v`  
  でrailsのバージョンが表示されれば完了(命令したディレクトリにgemfileがあると表示されないので注意)

##### STEP3:jekyll起動  
  `$ cd ~/cloudbase-static-page/docs`  
  `$ bundle exec jekyll s --baseurl ""`  
【※】/docs/(gemfileのある場所)でないと起動に失敗することに注意  
【※】_config.yml内のbaseurlによって起動がコントロールされている → ローカル上では見かけ上空白として起動するため 「""」と表記  

参考：[http://jekyllrb-ja.github.io/docs/installation/windows/](http://jekyllrb-ja.github.io/docs/installation/windows/)
