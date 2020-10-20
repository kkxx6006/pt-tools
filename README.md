## 20200829更新
1. 多站点多帐号支持

## 起源
在论坛入了一个PT小站玩玩，上传刷了1个T了，魔力有点难搞。 所以利用github action 做些奇奇怪怪的事情
## 适用
NuxusPHP 程序的PT站点，以后说不定支持其他程序
## 现在能干啥
1. 每天自动签到 +魔力
2. 每个小时自动对新种 say thanks +魔力
3. 顺带保号了，PT站一般有登录要求，签到顺带就登录了
## 咋用
0. Fork仓库
1. 添加CONFIG ， Settings > Secrets > New secret > CONFIG
2. 配置文件 config.ini [thanks_id] 项下内容删除，这里用来记录已经说谢谢的id

## CONFIG 这么设置
1. 下面例子内 所有’#‘后的内容删除 , 不能写注释
````
[
    {
        # 地址
        'url':'https://www.XXXX.com', 
        # cookie 执行从浏览器粘贴出来就行，不用处理，包在引号内就行
        'cookie':'__cfduid=d07c2c6b96d23b4a74c9f82b3bb55f9c1598353026; c_secure_uid=MjEwMA%3D; c_secure_pass=a7b591404ca1eb1ce113e26230988db; c_secure_ssl=eWVhaA%3%3D; c_secure_tracker_ssl=bm9wZQ3D%3D; c_secure_login=bm9ZQ%3D%3D',
        #执行哪些任务的列表 签到、说谢谢 
        'tasks':['sign_in','say_thanks'] 
	},

    # 如果还有其他站点，把上面的 配置复制一份，
    {
        'url':'https://www.QQQ.com', 
        'cookie':'__cfduid=d07c2c6b96d23b4a74c9f82b3bb55f9c1598353026; c_secure_uid=MjEwMA%3D; c_secure_pass=a7b591404ca1eb1ce113e26230988db; c_secure_ssl=eWVhaA%3%3D; c_secure_tracker_ssl=bm9wZQ3D%3D; c_secure_login=bm9ZQ%3D%3D',
        'tasks':['sign_in',] 
	}
]
````
## CONFIG 这么设置图

![Snipaste_2020-08-29_00-04-41.png](https://i.loli.net/2020/08/29/dFNHYPB3ZL1n28j.png)

## 然后看Action任务执行情况就行了

![微信截图_20200828152942.png](https://i.loli.net/2020/08/28/FkhS9TzgOCHlPYG.png)

![微信截图_20200828152957.png](https://i.loli.net/2020/08/28/gRt29zNAspMSeHm.png)


