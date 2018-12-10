[![Build Status](https://travis-ci.org/QianmiOpen/edge.png)](https://travis-ci.org/QianmiOpen/edge)
Edge --- Dubbo Visualized Testing Tool
========================
Welcome to Edgeex!
Edge是一款用于测试Dubbo接口的开发者测试工具；能够让开发者迅速对自己的dubbo服务进行界面化的测试；



使用指南

1. 在web容器中部署edge.war；
2. 获取待测dubbo服务的客户端jar包，例如：xx-api.jar
3. 将上述jar包放入${edge.home}/WEB-INF/third_lib目录中；
4. 修改${edge.home}/WEB-INF/config.properties，配置待测dubbo服务所在的注册中心；
5. 启动web容器；

1. edge中有些方法的params为“[null]”是为什么？
A：因为edge底层是使用反射技术实现，对于有些数据类型的展示逻辑还待优化。
2. edge中有些方法的params中常会出现key：null是为什么？
A：因为目前只能解析java基础数据类型string、list。无法解析自定义数据类型
3. dubbo api中有些入参是object，怎么传输？
A：object对象也是由java 基础数据类型组成，edge会把object解析为基础数据类型；
4. enum类型参数怎么传？
A：传int类型，对应关系为0,1分别顺序对于枚举类型
5. list类型参数怎么传？
A：接口需要传入list，那么传入格式为[[1,2]]或[["a","b"]]

![image](https://github.com/ofpay/edge/raw/master/main.jpg)
