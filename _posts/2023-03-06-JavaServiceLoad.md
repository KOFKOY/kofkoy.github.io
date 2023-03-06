---
layout: post
title: ServiceLoader
date: 2023-03-06 17:00:00 +0900
category: Java
---
# ServiceLoader 加载服务提供者

> 它是Java的SPI(Service Provider Interface)机制的一部分。 实现服务提供方 和 服务使用方解耦

### 实现原理
在ServiceLoader.load时 懒加载，根据传入的接口类，遍历META-INF/services目录下的以该类命名的文件中的所有类，并实例化返回。

### 使用
* 定义一个接口。
* 在 META-INF/services 目录下创建一个以该接口命名的文件。 包名+文件名
* 在该文件中定义接口的实现类。
* 使用 ServiceLoader.load 方法来加载并实例化类。