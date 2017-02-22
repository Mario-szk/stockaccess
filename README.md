# stockaccess


新手，没什么基础，第一次用python写，目的是解决自己工作中的问题，上市公司有很多财务数据，但并不能被股票分析软件所调用，尤其是历史数据。想要在股票分析软件上清析的查看历史财务数据是很因难，为此，写了这些代码，将公司历年来的财务数据导入到zccess数据库中，然后，股票分析软件就可以轻松调用了。

将上市公司分年度的财务数据，导入access数据库中，并被飞狐交易师，金字塔等股票软件调用

 清晰展示各上市公司的历年主要财务情况，并进行各种统计
 
参数1 ，rootdir,是数据源的保存地，其下有各类分年度的财务数据，为TXT格式
txt 文件名是  1990   1991   1992   1993等，里面有两列，1列是股票代码，2列是对应的财务数据

参数2，dbegin,dend是源数据的开始年份和终止年份，注意0标起点，dend=2016,是指处理到2015年

处理过程中会在rootdir中建立process     dest目录，最终的access数据库在dest目录中,每次处理前会清除  除了原始数据之外的数据

其他过程如下，1，删除上次数据，2创建process和dest目录 3合并分年数据  4生成股票代码文件 5拆分股票数据 6建库，6插入数据
还有什么不明白的，可以ricegene@gmail.com  或 QQ  83880572
