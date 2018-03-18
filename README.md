# one-click-line-echo
a one-click demo to deploy a line-echo bot to heroku

## auto deploy this demo

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## 這一個rep主要是memo一下怎麼在github上做一個可以讓自己，或別人one-click直接佈署到heroku的按鈕
## 相較於上一個[demo: one-click-flask-hello](https://github.com/maloyang/one-click-flask-hello)，這一個demo多了讓使用者輸入環境變數的功能
## 因為line bot一定要輸入你申請到的bot的"LINE_CHANNEL_SECRET"和"LINE_CHANNEL_ACCESS_TOKEN"，因此請確實輸入，這樣你的line-bot才會正常運作
- 如下，要加入這一段，就可以產生按鈕，可以參考[這邊](https://devcenter.heroku.com/articles/heroku-button)

<code>
  [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
</code>

- 接著是在你的repo上根目錄下放一個 app.json 檔，格式如下
- 因為這一次我們要加入環境變數，因此除了前三個是必要項，又加入了"env"這一個參數

<code><pre>
{
    "name": "flask line-bot echo demo",
    "description": "a basic line-bot with echo function base on flask @ heroku demo",
    "repository": "https://github.com/maloyang/one-click-line-echo",
    "env": {
        "LINE_CHANNEL_SECRET": {
          "description": "Input your 'Channel secret'"
        },
        "LINE_CHANNEL_ACCESS_TOKEN": {
            "description": "Input your 'Channel access token'"
        }
    } 
}
</pre></code>

- 只要完成了以上的事，就可以做一個快速佈署鍵給大家使用!!
- 以這一個demo為例，他會把你帶到heroku的畫面，假設你已經登入了，那動呈現的畫面如下

![line-bot-demo](https://imgur.com/V6UoAQY.png)

- 然後把你的app名稱、"LINE_CHANNEL_SECRET"、"LINE_CHANNEL_ACCESS_TOKEN" 就可以按"Deploy app"佈署囉!
- 當然以我這一個範例來說，你還需要在你的line develop channel的頁面上把你的heroku app的位址填進來，這樣line才知道要把訊息送到哪裡

![要填入callback的address](https://imgur.com/FPU4acI.png)


### 下一次再來記錄有加入add-on的deploy!
