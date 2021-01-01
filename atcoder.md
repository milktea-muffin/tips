# AtCoderに関するTips

## atcoder-cli

テストケースのダウンロード、テストの実行、コードの提出用CLI

- [atcoder-cliチュートリアル](http://tatamo.81.la/blog/2018/12/07/atcoder-cli-tutorial/)
- [online-judge-tools/oj](https://github.com/online-judge-tools/oj)

```sh
# インストール
$ pip3 install online-judge-tools
$ npm install -g atcoder-cli

# インストールの確認
$ acc -h       # accのインストール
$ oj -h        # ojのインストール
$ acc check-oj # accとojの連携
online-judge-tools is available. found at:
/Users/kayo/.pyenv/shims/oj

# accでatcoderにログイン
$ acc login
? username: milktea_muffin
? password: [hidden]
OK

# ojでatcoderにログイン WebDriverがないと言われる
$ oj login https://atcoder.jp/
# [INFO] online-judge-tools 11.1.1 (+ online-judge-api-client 10.7.1)
# [INFO] service recognized: AtCoderService.from_url('https://atcoder.jp/'): https://atcoder.jp/
# [NETWORK] GET: https://atcoder.jp/contests/agc001/submit
# [NETWORK] 302 Found
# [FAILURE] You are not signed in.
# [INFO] Trying to open Chrome via WebDriver...
# [ERROR] Message: 'chromedriver' executable needs to be in PATH. Please see https://sites.google.com/a/chromium.org/chromedriver/home

# [INFO] Trying to open Firefox via WebDriver...
# [ERROR] Message: 'geckodriver' executable needs to be in PATH.

# [INFO] Trying to open Edge via WebDriver...
# [ERROR] Message: 'MicrosoftWebDriver.exe' executable needs to be in PATH. Please download from http://go.microsoft.com/fwlink/?LinkId=619687

# [INFO] Trying to open Internet Explorer via WebDriver...
# [ERROR] Message: 'IEDriverServer.exe' executable needs to be in PATH. Please download from http://selenium-release.storage.googleapis.com/index.html and read up at https://github.com/SeleniumHQ/selenium/wiki/InternetExplorerDriver

# [INFO] Trying to open Safari via WebDriver...
# [ERROR] Message: Could not create a session: You must enable the 'Allow Remote Automation' option in Safari's Develop menu to control Safari via WebDriver.

# [INFO] Trying to open Opera via WebDriver...
# [ERROR] Message: 'operadriver' executable needs to be in PATH. Please see https://sites.google.com/a/chromium.org/chromedriver/home

# [ERROR] No WebDriver is available.
# [HINT] Please install a WebDriver.
# See https://www.selenium.dev/documentation/en/webdriver/driver_requirements/

# Detailed instructions:
#     If you use Ubuntu:
#         1. Run $ sudo apt install chromium-chromedriver firefox-geckodriver
#     If you use Ubuntu under Windows Subsystem for Linux:
#         1. Make a symbolic link from cookie.jar in WSL to cookie.jar out of WSL. For example, run $ ln -s /mnt/c/Users/%USERNAME%/AppData/Local/online-judge-tools/online-judge-tools/cookie.jar /home/ubuntu/.local/share/online-judge-tools/cookie.jar
#         2. Use `oj login` outside of WSL
#     If you use Windows:
#         1. Install Chocolatey. See https://chocolatey.org/
#         2. Run > choco install selenium-all-drivers

# [WARNING] Switch to use CUI-based login instead of Selenium
# [NETWORK] GET: https://atcoder.jp/contests/agc001/submit
# [NETWORK] 302 Found
# [NETWORK] GET: https://atcoder.jp/login
# [NETWORK] 200 OK
# Username: milktea_muffin
# Password:
# [NETWORK] POST: https://atcoder.jp/login
# [NETWORK] redirected to: https://atcoder.jp/home
# [NETWORK] 200 OK
# [WARNING] AtCoder says: × Welcome, milktea_muffin.
# [INFO] Welcome,
# [NETWORK] GET: https://atcoder.jp/contests/agc001/submit
# [NETWORK] 200 OK
# [SUCCESS] You have already signed in.
# [INFO] save cookie to: /Users/kayo/Library/Application Support/online-judge-tools/cookie.jar

# デフォルトで全ての問題のディレクトリを追加する設定に変更
$ acc config default-task-choice all

# 問題用ディレクトリの作成
$ acc new [contestID]

# テストケースの実行
$ oj t -c "python3 ./a.py" -d ./tests/
```
