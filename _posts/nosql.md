# 索引

组合索引({‘city’:1,‘district’:1}

base_info内嵌文档索引

price单索引

```java
db.insert_data.ensureIndex({ "city" :1,"district":1})
db.insert_data.ensureIndex({"base_info.types":1})
db.insert_data.ensureIndex(i"price":1})
   
   db.insert_data.find(i"base_info.types" : "6=1厅2卫"}).explain("executionStats")
db.insert_data.find({"city":"斑南" , "district" :"高新"}).explain("executionStats")
db.insert_data.find( {"city" :"北京" , " prsice" :{$lt:10000]}}) .explain("executionStats")

```

![image-20221205202249264](../img/image-20221205202249264.png)

# 题目 

vue-element-admin

## 第一题

![image-20221205210301376](../img/image-20221205210301376.png)

直方图，挑选一个type

![image-20221205195419996](../img/image-20221205195419996.png)

![image-20221205195000855](../img/image-20221205195000855.png)



![image-20221205201501276](../img/image-20221205201501276.png)





## 第二题

![image-20221205210348218](../img/image-20221205210348218.png)

折线图

## ![image-20221205195008868](../img/image-20221205195008868.png)

## 第三题

![image-20221205210359287](../img/image-20221205210359287.png)

两个城市，分别展示

![image-20221205195206993](../img/image-20221205195206993.png)

## 拓展

### 1

![image-20221205195249783](../img/image-20221205195249783.png)

### 2

*![image-20221205201053494](../img/image-20221205201053494.png)*

![image-20221205201116138](../img/image-20221205201116138.png)

### 3

![image-20221205210426850](../img/image-20221205210426850.png)

![image-20221205202103892](../img/image-20221205202103892.png)



### 4![image-20221205202550249](../img/image-20221205202550249.png)

# neo4j

房屋house：area面积、maintain、

district区域

lease_mode

direction

region

elevator

water

electricity

washing_machine

air_condition

wardrobe

tv

refrigerator

heater

bed

broadband

gas

MATCH (p1:houser {_id: '628c6014b81ebb7a531422bf'})
MATCH (p2:houser {_id: '628c7c7505574caf26abed73'})
RETURN algo.linkprediction.adamicAdar(p1, p2, {relationshipQuery: 'is'}) AS score