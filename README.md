#一个简单的豆瓣信息爬虫
##一、豆瓣同城数据爬取

目标网址：http://www.douban.com/location/xian/

1. 抓取豆瓣同城栏目所有有关的活动信息，具体指标如下：
	1. 抓取西安、北京、上海、武汉等城市
	2. 抓取同城的音乐类、戏剧、讲座、聚会、电影、展览、运动、公益、旅行、其他等
	3. 每一个活动需要获取：活动名称、活动id、时间、地点、费用、类型、主办方、感兴趣的人、参加的人等（其中感兴趣的人以只需抓取人名对应的uid）

2. 数据存储格式要求：
	1. 每一个活动以一个txt文件存储，文件名命名规则为“地名\_活动类型\_活动id.txt”
	2. 文件内，以上各个字段分别各占一行，其中参加及感兴趣的人的uid单独一行，uid之间以逗号（英文逗号）分隔。

##二、豆瓣线上活动抓取
目标网址：http://www.douban.com/online/

1. 抓取所有线上活动（可以标签为索引）
2. 具体指标：
    1. 抓取每一个线上活动的标题及活动id
    2. 获得每一个活动的发起者以及所有参与者的uid
    3. 数据存储格式要求：
        1. 所有活动存储在一个txt文件中
        2. 每一行代表一个活动
        3. 每一行至少分为四个字段，第一个字段为活动id，第二字段为活动名称（活动名称中去除所有标点符号），第三字段为发起人的uid，第四字段及以后为参与人uid 
        4. 字段之间用逗号（英文逗号）隔开。


