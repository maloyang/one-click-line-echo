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

- 接著是在你的repo上根目錄下放一個 app.json 檔，格式：
- 其實也只有前三個是必要的，可以看一下目前這一個「one-click-flask-hello」repo內的app.json檔就會了解
<code><pre>
{
  "name": "Node.js Sample",
  "description": "A barebones Node.js app using Express 4",
  "repository": "https://github.com/heroku/node-js-sample",
  "logo": "https://node-js-sample.herokuapp.com/node.png",
  "keywords": ["node", "express", "static"]
}
</pre></code>

- 只要完成了以上的事，就可以做一個快速佈署鍵給大家使用!!

### 下一次再來記錄有加入add-on的deploy!
