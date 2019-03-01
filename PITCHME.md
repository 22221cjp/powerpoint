# SES Bounce Rate&Complaint Rate
---
#### Bounce Rate&Complaint Rate
![](resources/7AA5DBFFCA2529E863B7DDCBAC669E90.jpg)
---
**Bounce Rate&Complaint Rate**
* Bounce Rate – 邮件的退回率，收件邮件地址无效率。
* Complaint Rate - 总体投诉率
---
**什么是投诉？**

当收件人报告他们不想接收某封电子邮件时就出现了投诉。他们可能单击了其电子邮件客户端中的“报告垃圾邮件”按钮，向其邮件提供商投诉，直接或通过某种其他方式通知 Amazon SES

**如果 Amazon SES 账户的总体退回邮件率超过 10% 或 Amazon SES 账户的总体投诉率超过 0.5%，则 Amazon SES 账户会自动置于审核状态。**
---
**解决--SNS&SQS**

* SNS（Simple Notification Service）
类似于MQ中的Topic，publish发布消息后，多个订阅终端都能收到通知。
不同的地方在于：**不支持消息堆积**，所以需要搭配SQS使用

---
**SNS(Simple Notification Service)**
![IMAGE](resources/CA4BBBFFA0DB4A5B8C23FE90BD7A834B.jpg =602x387)

---

---
2. 没有命中一级缓存的团单改为批量调用后端服务（稍复杂）
3. 当团单数据多的时候，后端全量内存缓存可能需要改为redis
