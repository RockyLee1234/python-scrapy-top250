# python-scrapy-top250
njupt 数据处理实验code分享
主要思路：
第一部分，利用python scrapy爬取豆瓣top250的具体数据，包括排名、导演 、主演、热评、评价人数、评分等，爬取完成后保存在data.csv文件中。
Ps:对于豆瓣包括但不限于限制ip频繁访问的反爬虫机制，一方面需要对下载中间件进行一些伪装设置，包括使用IP代理和代理user-agent方式，在middlewares.py文件中新建一个user_agent类用于为请求头添加用户列表；另一方面，在setting.py文件中通过更改参数，降低访问频率，从而通过检测
第二部分，先把data.csv文件转化为data.xlsx,再利用python和excel基本功能对数据进行基本的清洗以及整理
第三部分，利用python pandas、matplotlib,jieba,进行数据的分析以及可视化处理。个人在这一部分的操作包括：得到comments降序排序后与star的折线图、ranking与star的折线图从而分析出热度、品质与电影评分的相互作用关系，另一方面对于热评、导演、主演进行关键词统计，并且建立词云，从而得出不同电影类型的受欢迎程度、以及top级别电影所反映的高水平导演、高水平演员。
