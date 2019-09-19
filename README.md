# Network-Final-Project
## 專題說明
* 使用packet tracer實作
* 每個城市有一個對外的router (port: 接到外面+兩棟樓router)
* 一個城市裡有兩棟樓
* 每棟樓中有n個部門 (1個router接n個switch)

## 分配說明
### 分給8個部門 2^3  

11100000 -> 每個部門可以分配給29個使用者(2^5=32, 32-3=29)  
子網段: 255.255.255.224  
反向遮罩: 0.0.0.31  
每個網段中設備的ip address: 10.0.0.x/27  
![image](https://github.com/fairy990524/Network-Final-Project/blob/master/detail_1.PNG)


### 分給4個部門 2^2
11000000 -> 每個部門可以分配給61個使用者(2^6=64, 64-3=61)  
子網段: 255.255.255.192  
反向遮罩: 0.0.0.63  
每個網段中設備的ip address: 11.0.0.x/26 (11~13.0.0.x/26)  
![image](https://github.com/fairy990524/Network-Final-Project/blob/master/datail_2.PNG)


### wifi設置
有wifi的 ip設前十個 所以server ip +10 or 第一個ip (wifi只能連到wifi機所在的server)  
若有printer 會給他一個ip  


### 兩個router間的連線:
11111100  
子網段: 255.255.255.252  
反向遮罩: 0.0.0.3  
第一個網段 192.168.1.0 : 可以提供4-2=2個router ip (192.168.1.1/30 & 192.168.1.2/30)  
所有router的網段: 192.168.x.0 (x=1~5)  
