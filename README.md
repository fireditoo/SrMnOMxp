# 前言

欢迎来到本项目的Gitee页面。这是一个基于个性化推荐的外卖点餐系统，是Java计算机毕业设计分享项目之一。该系统利用了当前流行的技术，旨在为用户提供便捷、个性化的点餐体验。下面将详细介绍本项目的相关内容。

## 内容介绍

本项目是一款基于Java开发的在线外卖点餐系统，其主要特色是引入了个性化推荐功能。用户可以根据自己的口味、历史订单等数据，获取到最符合个人需求的美食推荐。系统不仅为用户提供了便捷的点餐体验，还为商家带来了更精准的销售策略。此外，系统具有良好的可扩展性，方便后期进行功能升级和维护。

## 技术介绍

本项目采用以下技术栈进行开发：

- **语言：** Java
- **使用框架：** Spring Boot
- **前端技术：** JS、Vue、CSS3
- **开发工具：** IDEA/Eclipse
- **数据库：** MySQL 5.7/8.0
- **数据库管理工具：** phpstudy/Navicat
- **JDK版本：** jdk1.8
- **Maven：** apache-maven 3.8.1-bin
- **前端环境：** Node.Js 12\14\16

## 核心代码

以下是本项目中的一段核心代码，展示了如何实现个性化推荐功能：

```java
// 根据用户历史订单数据，推荐菜品
public List<Dish> recommendDishes(String userId) {
    // 查询用户历史订单
    List<Order> orderList = orderService.getOrderListByUserId(userId);
    
    // 统计用户口味
    Map<String, Integer> tasteMap = new HashMap<>();
    for (Order order : orderList) {
        List<Dish> dishList = order.getDishList();
        for (Dish dish : dishList) {
            String taste = dish.getTaste();
            tasteMap.put(taste, tasteMap.getOrDefault(taste, 0) + 1);
        }
    }

    // 根据口味推荐菜品
    List<Dish> recommendList = new ArrayList<>();
    for (Map.Entry<String, Integer> entry : tasteMap.entrySet()) {
        String taste = entry.getKey();
        List<Dish> dishes = dishService.getDishesByTaste(taste);
        recommendList.addAll(dishes);
    }

    return recommendList;
}
```

## 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

# 项目截图

![封面图片](https://img10.360buyimg.com/ddimg/jfs/t1/338620/10/7834/179980/68bc5c7bF8399342c/c150c48e144865ee.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/327852/36/16845/128199/68bc5c5bFb30eb2d5/bd7bbf88c4201dd9.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/331070/13/10043/75615/68bc5c5bF30641509/b26965020447ad33.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/299173/39/16328/48676/68bc5c5cF5cc4db84/4c9ec654fbfc1d2e.jpg)

![介绍图片](https://img11.360buyimg.com/ddimg/jfs/t1/288087/21/20601/48709/68bc5c5dF666aee68/99296657039883aa.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/328221/31/17058/53405/68bc5c5eFa813c896/6dbd0700b4c1a635.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/345961/38/459/47814/68bc5c5eF5e36343d/1945e516807b6c42.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/323825/31/17180/23225/68bc5c5fF027f8394/ae6ec25c4d83e0ba.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/344158/13/475/33769/68bc5c5fFcf22a9b0/190f434e7e7af080.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/334627/10/10162/62400/68bc5c60Fe5b063e2/ddad83319aa879f2.jpg)


## 万字文档
![文档介绍](https://img14.360buyimg.com/ddimg/jfs/t1/338393/1/3576/156947/68b1ad0cF74dc525c/ff9cd6c574295685.jpg)
