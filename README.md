# Get-Free-SS

脚本现在支持爬取 SS 和 SSR 两种数据。客户端软件下载请到 GitHub 搜索 `shadowsocks-windows` 或者 `shadowsocksr-csharp`。

## 📜功能
自动爬取网络上公开的免费 SS、SSR 账号密码，并写入本地文件中，如果 `config/index.js` 文件中设置了 `url` 的值，则会自动替换掉软件中旧的账号。

## ⚙设置
本脚本需要访问 `www.youneed.win` 网站，如果你的电脑无法打开此网站，那么需要修改HOST文件。
1. 目录：C:/Windows/System32/drivers/etc，用记事本打开host文件
2. 在最后添加并保存下面的内容
    ``` bash
    # FQ start
    104.31.74.55 youneed.win
    104.31.74.55 www.youneed.win
    104.18.18.18 free-ss.site
    # FQ end
    ```
3. 进入命令行(win+R 输入cmd回车)，执行：ipconfig /flushdns
4. 重新刷新页面即可,如失效请还原host并用代理访问

## 🎡使用
本脚本使用了 `node` 和 `npm`。

``` bash
# 1. 检查 node 和 npm，如果都有输出版本号，则可以进行下一步，否则请自行安装node
node -v
npm -v

# 2. 下载或使用 git clone 本项目到你的电脑
git clone https://github.com/maxmeng93/Get-Free-SS.git

# 3. 进入脚本目录
cd Get-Free-SS

# 4. 安装依赖
npm i

# 5. 配置 config ，如果不需要自动替换软件中的旧的SS账号，则此步骤可以省略
# 打开 config/index.js 文件，url 设置为你的文件路径，

# 6. 执行
npm start

# 7. 查看 data 文件夹中生成的文件
```

## 👀注意
* 配置 config 文件中的 url 时，一定要注意路径的斜杆必须转义。
* 如果需要替换 `gui-config.json` 中的账号密码配置，请确保已经启动过软件，并已生成配置文件（可以通过修改设置、添加节点等方式生成配置文件）。

## 📢说明
网络中的内容良莠不齐，请合理使用本脚本。
