# SES Bounce Rate&Complaint Rate
---
#### Bounce Rate&Complaint Rate
![](resources/7AA5DBFFCA2529E863B7DDCBAC669E90.jpg)
---
Bounce Rate&Complaint Rate
## Bounce Rate – 邮件的退回率，收件邮件地址无效率。
## Complaint Rate - 总体投诉率



###什么是投诉？

当收件人报告他们不想接收某封电子邮件时就出现了投诉。他们可能单击了其电子邮件客户端中的“报告垃圾邮件”按钮，向其邮件提供商投诉，直接或通过某种其他方式通知 Amazon SES

###如果 Amazon SES 账户的总体退回邮件率超过 10% 或 Amazon SES 账户的总体投诉率超过 0.5%，则 Amazon SES 账户会自动置于审核状态。
---
目前提供给搜索的接口为：
BeautyStructureServiceImpl#loadAllBeautyDealTag(final List<DealTagArgs> dealTagArgs)

之前优化的wiki：http://wiki.sankuai.com/pages/viewpage.action?pageId=491621043
---
接下来可能的工作：
1. poi变更可能的影响
  >搜索接口有根据商户类别过滤团单类别的逻辑。
  美发（157）：从二级分类变为三级。跟产品确认中：
  如果已有的商户类别不会变更，只是新增的商户可能有新的类别，对目前搜索接口没有影响
  如果已有的美发商户可能改为养发健发，这个有一点影响。
  美甲（160）：分类和原来相同，无影响
  美容（158）：同美发
  即使有影响，代码调整不大，很快能够改好

![](resources/4A62F6FAB93FC6A128346FD010EA2219.jpg)
---
2. 没有命中一级缓存的团单改为批量调用后端服务（稍复杂）
3. 当团单数据多的时候，后端全量内存缓存可能需要改为redis
