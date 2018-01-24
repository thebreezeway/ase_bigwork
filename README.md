外网访问地址：https://stormy-ridge-75886.herokuapp.com
# HousePricing

HousePricing旨在提供房价的可视化预测，帮助用户更好的评估房产和预测未来的价格

### 1. 面向用户(买房者、卖房者)

对于买家，在主页面通过各种筛选选出符合条件的房屋，进入各个房屋的详细页面，应用通过各种可视化手段让用户从交通、教育、工作、交通、生活等方面对这套房子进行评估。

新增功能：
    1.房源历史数据展示
    2.用户登陆注册功能

### 2. 面向开发者（数据挖掘工程师，数据可视化分析师等）

如果你是面向地理位置的数据挖掘工程师，你可以不用编写与百度API交互的代码，直接运行这个应用后导入自己的房屋数据，应用会自动与百度API爬取周围的基础设施，获得的数据可用来作为学术研究和分析等

请点击这里查看详细信息:http://blog.csdn.net/ppp8300885/article/details/77806852




## 截图



<img src="/lib/bigwork1.png">

<img src="/lib/bigwork2.png">

<img src="/lib/bigwork3.png">

<img src="/lib/bigwork4.png">

## 数据说明

在房源house_table添加spider_status字段，用来记录房屋周边爬取进度
添加历史数据表，用来记录房源历史价格数据



## 开发

原始数据由[scrapy-hoursepricing](https://github.com/ParadoxLiu/bigwork/tree/master1/spider/__init__)爬取，抓取后的数据将存为json格式，然后由HousePricing进行解析并储存在数据库中

本项目由rails框架开发，请自行安装相关环境，请先fork此项目，然后运行下面：

```
git clone your_forked_project
cd project_path
bundle install
rake db:migrate
rake db:seed
```

在浏览器中输入`localhost:3000`，即可访问主页

**若需要原数据（我目前用的数据），请导入根目录下的`mydb.dump`到postgresql数据库**


