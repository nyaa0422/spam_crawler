# spam_crawler

- 各スパム確認サイトを巡回するだけのスクリプト(最新版)
- 入力はip.xlsxのA行のip  
- 出力はresult.xlsx  


■環境
python3.11, windows10 64bit
ライブラリ
selenium openpyxl 
(多分2つだけ)

■環境構築
1. python3.11インストーラをを公式サイトからダウンロードしてpythonをインストール
https://www.python.org/ > Downloads > Download for Windows から最新版のpythonをダウンロード
2. ライブラリをインストール
コマンドプロンプトを開き、以下を実行
#pip install openpyxl selenium

■操作手順
1. ip.xlsxを作成し、1列目に調べたいip列を貼り付けて保存した後閉じる
2. result_template.xlsxを複製してresult.xlsxとしてリネームする
3. crawler.pyのあるディレクトリに移動し、以下のようにcralwer.pyを実行する
#python .\cralwer.py
4. 終了したらresult.xlsxを開いて結果を確認する

※注意事項
- このスクリプト実行中でエラーが出たIPは空白になるので手動で埋める必要あり
- スクリプトを実行中にxlsxファイルを開くとエラーでスクリプトが止まる可能性があるので注意(最初からやり直し)
- chromeのバージョンがある程度新しくなるとこのスクリプトが動かなくなるので、
- 適宜今のchromeバージョンにあったchromedriver.exeをダウンロードする

↓バージョン違いでこのようなエラーがでる\\
Current browser version is 123.0.6312.60 with binary path C:\Program Files\Google\Chrome\Application\chrome.exe

- 以下最新版chromedriver.exeのダウンロード場所
- win64のchromedriverをダウンロード
https://googlechromelabs.github.io/chrome-for-testing/

