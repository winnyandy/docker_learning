# docker_learning

## Download docker images
```bash
docker pull ubuntu
```

如果要特定版本
```bash
docker pull ubuntu:14.04
```

通常下載image不打網址，會使用預設倉庫，如要特定倉庫
```bash
docker pull dl.dockerpool.com:5000/ubuntu
```

讀取image建立容器(instance)
```bash
docker run -it ubuntu bash

參數詳解
-i:   讓容器的標準輸入保持打開

-t:   分配一個虛擬終端(pseudo-tty)並綁定到容器的標準輸入
```

查看image資訊
```bash
docker images
```

搜尋想要的image列出清單
```bash
docker search XXX
```

刪除image
```bash
docker rmi [ dl.dockerpool.com:5000/ubuntu / ID ]
```
在A的image裡變更內容並產生新的image
```bash
docker commit -m "describe something" -a "XXX" [image ID] [image NAME]
```

打包image並產生一個檔案
```bash
docker save -o [output name.tar] [save image name]
```

載入image.tar檔案至docker中
```bash
docker load --input [image name.tar]
```
上傳docker image 至 docker Hub
```bash
docker tag [image name:latest] [tag name:latest]
docker push [tag name:latest]
input:
      Username
      Password
      Email
 ```

建立容器(instance)
```bash
docker create -it ubuntu:latest
```

