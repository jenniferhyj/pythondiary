# pythondiary

## 專案介紹

我想做個網站!

## 成品展示:

![實際畫面](https://github.com/jenniferhyj/pythondiary/raw/master/%E7%B6%B2%E9%A0%81.png)

[網站網址](https://final0817--jennifer0625.repl.co/)

## 使用技術

工具名稱 | 用途
---------|----------
Python 3 | 不需要解釋
Flask(python)    | 幫助我建立伺服器
HTML/CSS  | 網頁表示和排版
Heroku   | 託管網頁
Github   | 存放原始碼






##程式碼片段
```python
@app.route("/")
def home():
    temp = glob.glob("articles/*")
    fill = []
    for t in temp:
        length = len(glob.glob(t + "/*.txt"))
        category = t.replace("articles/", "")
        f = (category, length)
        fill.append(f)
    return render_template("index.html", cat=fill)

app.run(debug=True, host="0.0.0.0", port="3000")
```
