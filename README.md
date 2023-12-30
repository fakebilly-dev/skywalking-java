# Monet SkyWalking Java Agent
## v8.9.0

## 自定义插件
### monet-log-plugin
- 适配 Logback 链路
- 适配 Log4j2 链路
- 适配 ```ThreadPoolExecutor.execute``` Lambda 表达式
- 适配 ```ThreadPoolExecutor.submit``` Lambda 表达式

## 构建

### 中文社区指引
> https://skyapm.github.io/document-cn-translation-of-skywalking/zh/8.0.0/guides/How-to-build.html#
### Apache 发行版本源代码构建
```
# 构建命令
./mvnw clean package -DskipTests
```

## 跨线程
- 适配 ```ThreadPoolExecutor.execute``` Lambda 表达式
- 适配 ```ThreadPoolExecutor.submit``` Lambda 表达式
### 使用方式
1. 构建 ```skywalking-agent/```
2. 移动 ```skywalking-agent/bootstrap-plugins/apm-jdk-threading-plugin-8.9.0.jar``` 至 ```skywalking-agent/plugins/apm-jdk-threading-plugin-8.9.0.jar```
3. 服务启动命令 指定 ```-Dskywalking.plugin.jdkthreading.threading_class_prefixes=[YOUR_APPLICATION_ROOT_PACKAGE]```
