# upload-download-java

![size](https://img.shields.io/github/repo-size/myifeng/upload-download-java)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/myifeng/upload-download-java/Java%20CI%20with%20Gradle)
![license](https://img.shields.io/github/license/myifeng/upload-download-java)

🌍
*[English](README.md)  ∙ [简体中文](README.zh-CN.md)*

**Java语言开发的文件上传和下载通用模块**

**脱离具体业务场景，上传成功后返回一个文件路径的数组，开发者可以决定如何去使用该路径。**

## 环境

- JDK 11

- Gradle 7.0.2

- Spring Boot 2.5.1

## 用法

- ### 上传文件
``` http request
POST /appendix/test
Content-Type: multipart/form-data; boundary=WebAppBoundary

--WebAppBoundary
# File upload
Content-Disposition: form-data; name="file"; filename="demo.tar.gz"
Content-Type: application/x-gzip

# Here you specify file to upload
< ../../tar/demo.tar.gz
--WebAppBoundary--

# return a collection of file paths
["\\appendix\\test\\daad5d07-2be6-44fa-978c-1581931a63a2\\demo.tar.gz"] (Windows)
["/appendix/test/daad5d07-2be6-44fa-978c-1581931a63a2/demo.tar.gz"] (Linux/MAC OS)
```

- ### 获取文件

```http request
GET /appendix/test/daad5d07-2be6-44fa-978c-1581931a63a2/demo.tar.gz
```
## 相关工程

- [upload-download-nodejs](https://github.com/myifeng/upload-download-nodejs) - Node.js语言开发的文件上传和下载通用模块.

## 维护者

[@myifeng](https://github.com/myifeng).

## 贡献代码

遇到问题请[创建issue](https://github.com/myifeng/upload-download-java/issues/new) ,也欢迎提供代码提交PR

贡献代码的规范和标准请参阅 [Contributor Covenant](http://contributor-covenant.org/version/1/3/0/).

## 贡献者

非常感谢以下所有的贡献者：

[![All contributions](https://contrib.rocks/image?repo=myifeng/upload-download-java)](https://github.com/myifeng/upload-download-java/graphs/contributors)

## 使用许可

[MIT](LICENSE) © myifeng

