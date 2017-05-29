欢迎使用@Foldblade 编写的、基于Python的比特币邮件提醒系统。  

## 开发的原因：  
因为本人还是个在校高中生，并无过多的时间关注比特币行情（想炒btc还不是因为家长闹离婚得尽快想办法养活自己）——但还是被允许有时间处理个人邮件。所以，编写此python程序，以满足个人需要——每日整理行情发送邮件。  
水平有限，作为学习Python以来编写的除“Helloworld”后第二个程序，代码可能过于弱智，在此班门弄斧，诚惶诚恐。  
仍望海涵！  

## 本人环境：  
`Python 3.5.3`  
`CentOS 6.6`  
**建议将系统调为中文环境，某些输出可能涉及中文**

## 已经实现的功能：
- BTC、ETH、LTC的支持
- 邮件发送
- 汇报平均值、方差、极差、最大最小值
- 绘制24小时内比特币价格折线图

## 具体配置：
主要分为以下两个部分：
- 数据抓取部分
- 邮件发送部分

**使用前请在dailymail.py内配置好邮件服务器和接收邮箱！！！**
日后会加入数据分析…… 
数据抓取部分，每分钟从交易网站抓取价格，并以csv格式记录。  
请注意，/data/pricelog.csv用文本编辑器打开应该是1441行。
在Linux上，我用crontab来每分钟执行一次。  
邮件发送部分，源代码里的注释里已经配置好了一个邮件服务器。如果您还没有合适的邮箱，可以选用注释里我的邮箱来进行发件。  
然后依旧用crontab来定时，譬如每天21:00发送一次邮件。

请注意：每次更新后，可能需要等待24小时来恢复正常状态。请耐心等待。

### 更新：
- 2017.5.29
  - 支持BTC、ETH、LTC记录、绘图
  - 邮件支持多附件，用HTML表格形式汇报
  - 邮件更注重隐私，为每个收件人单独发送邮件

- 2017.4.4
  - 汇报平均值、方差、极差、最大最小值
  - 邮件附图加入平均值，x轴支持显示时间

enjoy ^_^
