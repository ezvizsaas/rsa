# 说明
saas组件消息推送解密sdk，三方订阅企业萤石云消息，对消息进行RSA加解密的库

#如果是JAVA语言
建议直接下载源码，引入项目文件中

#如果是C#
建议下载rsa-1.0.0.jar和commons-codec-1.11.jar，之后再使用IKVM.NET，依次将commons-codec-1.11.jar包转成commons-codec-1.11.dll动态链接库
之后再在控制台执行命令：
ikvmc out:RsaNetXXXX.dll rsa-1.0.0.jar -r:commons-logging-1.1.3.dll
这样打出来的RsaNetXXXX.dll动态链接库中才能将commons-logging-1.1.3.dll库引用进去

#如果是NodeJS
const publicKey = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
let NodeRSA = require('node-rsa')
const key = new NodeRSA(publicKey, 'pkcs8-public');
console.log(key.decryptPublic(jsonData, "utf8"))




