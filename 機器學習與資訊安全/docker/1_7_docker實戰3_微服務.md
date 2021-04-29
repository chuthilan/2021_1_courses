
#
```
https://ithelp.ithome.com.tw/articles/10209304
```
### application
```
package main

import (
    "fmt"
    "log"
    "net/http"
)

func main() {
    http.HandleFunc("/ping", func(w http.ResponseWriter, r *http.Request) {
        fmt.Fprintf(w, "Hello World")
    })

    log.Fatal(http.ListenAndServe(":8080", nil))
}
```
### dockerfile
```
FROM golang:1.11.2-alpine
WORKDIR /helloworld
ADD . /helloworld
RUN cd /helloworld && go build
EXPOSE 8080
ENTRYPOINT ./helloworld
```
###
```
//這邊是做 image 建立的動作 大家可以把 yourname 取代成自己想要名稱，後面則為你的專案名稱
docker build -t yourname/helloworld .

//這邊就是執行 image 讓他成為 container， --rm 代表執行完接著刪掉 container -p 代表把 cotainer 的 port 對接到你本機的實體 port
docker run --rm -p 8080:8080 -d yourname/helloworld


使用瀏覽器訪問 http://127.0.0.1:8080/ping 就能看到 Hello World 。
```
