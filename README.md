中国新闻爬虫
=======

默认从以下网站获取新闻：
========

中国新闻网(ZXW)

网易新闻(163)

人民网(RMW)

新浪(SINA)

凤凰资讯(IFENG)


配置（在GetChinaNews.py中修改）：
==
defaultSiteList = ["ZXW","163","RMW","SINA","IFENG"] #新闻源站点设置，默认5个站点都获取

argD = os.getcwd()+os.path.sep+'dataNews'#抓取的新闻目录设置

命令执行说明：
==
python GetChinaNews.py  获取当天新闻（对于163和RMW这个无效，因为它们的滚动新闻页面没有当天的）

python GetChinaNews.py -d 2013-11-12  获取2013-11-12这一天的新闻

python GetChinaNews.py -d 2013-11-12 2013-11-14 获取2013-11-12到2013-11-14之间的新闻

python GetChinaNews.py -dx 2013-11-12 5 获取2013-11-12之后5天的新闻

python GetChinaNews.py -a 获取最近30天内的新闻
