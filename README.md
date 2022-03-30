# 安装
钉钉群机器人设置为 "加签" 验证

`go get -u github.com/songjuncai1122/dingdiing`

# 使用
`
d := dingding.Webhook{
AccessToken: "8c03f234ddf2axxxxxxxxxxxx",
Secret:      "SECefded9b38b761fxxxxxxxx",
}
err := d.SendMessage("这是普通的群消息")
`
# at特定的人
`
d := ding.Webhook{
AccessToken: "8c03f234ddf2axxxxxxxxxxxx",
Secret:      "SECefded9b38b761fxxxxxxxx",
EnableAt:    true,
}
err := d.SendMessage("Harvey, 你的程序挂了", "1856362xxxx")
...
err = d.SendMessage("Harvey, Bob 和 Bella, 你们的程序挂了", "1856362xxxx", "1867800xxxx", "1715372xxxx")
`
# at所有的人
`
d := ding.Webhook{
AccessToken: "8c03f234ddf2axxxxxxxxxxxx",
Secret:      "SECefded9b38b761fxxxxxxxx",
EnableAt:    true, // 开启艾特
AtAll:       true, // 艾特所有人
}
`
