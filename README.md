# Softflowd
## 說明
本程式主要處理用 Netflow 轉成 NSL-KDD 所需之格式
### [Source Code](softflowd-0.9.9.tar.gz) 

### 前置套件
#### Ubuntu
``` sh
sudo apt install gcc libpcap-dev
```
#### CentOS
``` sh
sudo yum install gcc libpcap-devel
```

### 執行
``` sh
chmod +x softflowd 
sudo softflowd -i ens33 -n localhost:9999 -v 9 -s 0 -t maxlife=2 -D | grep EXPIRED
```

## How to Recompile
``` sh
rm -rf softflowd Makefile # 舊的結果先刪除
./configure # 生出 Makefile
make # 生成輸出檔
sudo make install # 整合成執行檔
```
