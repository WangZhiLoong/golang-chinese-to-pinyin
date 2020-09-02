你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
golang-chinese-to-pinyin
========================

中文转拼音golang实现

install
--------
```
go get github.com/l2x/golang-chinese-to-pinyin
```


example
--------

```golang
package main

import (
    "fmt"
    "github.com/l2x/golang-chinese-to-pinyin"
)

func main() {
    s := "天气不错"

    py := Pinyin.New()
    p, _ := py.Convert(s)

    fmt.Println(p)
    //Tian Qi Bu Cuo


    //设置分隔符
    //首字母是否大写
    py.Split = "-"
    py.Upper = false
    p, _ = py.Convert(s)
    fmt.Println(p)
    //tian-qi-bu-cuo
}
```
