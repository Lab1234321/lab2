#Log
===

###Log Tue Apr 19 CST 2016
#####What is accomplished?
1. 与客户代表进行访谈，了解并获取需求信息
2. 建立git仓库，用来保存和更新需求分析文档
3. 整理访谈结果

#####What to do next?
1. 列举在需求获取和分析过程中所发现的各种问题，逐条说明本小组是如何解决这些问题的
2. 确定系统开发总体目标
3. 完成用况模型的建模

===

###Log Tue Apr 19 CST 2016
#####What is accomplished?
1. 根据得到的需求信息制作了DFD0层图和DFD1层图

#####What to do next?
1. 根据制作完毕的DFD1层图进一步制作DFD2层图

#####Some feelings
1. 原来用的StarUML，感觉十分方便顺手，可是这次做DFD没法用StarUML，只好再下个Visio（而且组员用的也都是Visio，我想看他们的图也只能下个Visio了），下载后发现这个软件与StarUML相差很大，用手画了十分钟的图，硬是用了好几个小时才在Visio上画完，而且整体效果也不是很好，以后还要更多的学习相关建模软件的使用，提高效率
2. 需求的分析一定要详细具体，我们在初次采访后完成的需求分析中还是有很多不足之处，如终端功能中的“扫书”，并没有说明是录入书籍信息还是借还书，对网上功能操作的描述也不确定（没有完全描述其功能要求，而使用了“等”），这些都是我们之后需要改进的方面
3. 对于1中提到的需要下载Visio才能看到别人的建模图，我认为对于团队合作进行需求建模时，还是最好要另外上传一份图片格式的建模图，方便其他组员进行查看


===

###Log Wed May 4 CST 2016
####What is accomplished?
1. 发现了一些需求中的模糊处：
	* 读者对于网上用户功能的阐述中提到“进行预约，查询等操作”，后经分析核实，读者网上登录可以进行的操作有：预约图书，查询图书信息，修改读者信息
	* 前台代表和财务代表对于违约金收取方式的阐述有分歧。前台代表认为“只接受现金，不接受网上支付”；财务代表则认为“支付形式可有现金，支付宝，刷卡”<br>
	并对相应的文档做出了修改
2. 对类图的设计进行了一些讨论：<br>
	// TODO 预约的职责分给哪个类？等问题

####What to do next?
1. 讨论状态机图，并做相应更改
2. 检查是否仍有不明确的地方

####Questions and Answers
1. 新书录入是由哪个部门负责？<br>
	后台管理人员负责录入
2. 违约金缴纳方式有哪些？是否接受网上支付？<br>
	现金 第三方 银行
3. 终端能不能预约图书？<br>
	能
4. 维护人员可以修改图书的馆藏地点，那前台是否可以修改？如果前台不能修改的话，那么预约服务是否需要维护人员参与更新馆藏信息？<br>
	前台不可以
5. 读者在网上登录时可以进行哪些操作？之前的采访中只提到了预约，查询等操作，请问查询的内容具体包括哪些（预约信息／借阅历史／违约信息／当前外借书目）？还有是否需要其他操作，比如修改读者信息？<br>
	这些应该都能查询。可以修改联系方式和密码

===

###Log Thu May 5 CST 2016
####What is accomplished?
1. 对状态机图的具体实现进行详细的讨论，并进一步完善修改
2. 对用例图进行修改

####What to do next?
1. 修改类图
2. 画泳道图
3. 进一步完善状态机图细节部分

####Questions and Answers
1. 修改个人信息是否跟前台相关？<br>
	可以去前台那里修改
2. 读者证挂失、修改个人信息、管理预约书籍等服务是否可以在自助终端上完成？<br>
	可以，预约书籍的存放，新增，取走，到期全部由前台管理
3. 借书／还书／预约的流程<br>
	流程就是正规的流程
4. 前台能否查询预约信息／借阅历史／违约信息／当前外借书目等信息？<br>	可以
5. 已经被标记为缺失且交了赔偿金的书又还回来了，是拒绝接受，还是接受，还是接受并退款？<br>
	不接受

===

###Log Fri May 6 CST 2016
####What is accomplished?



####What to do next?
1. 继续完成状态机图
2. 整理一下需求中模糊遗漏的部分，并做成文档
3. 将以经核对过的建模结果整理到需求文档中
4. 整理Log

####Discussion
1. 读者证的挂失问题：
	之前类图中没有做读者证这个类，但是在画状态机图的过程中发现，挂失的流程需要区别同一个读者在不同时间办理的读者证，从而让旧的读者证失效，重新办理新的读者证。经过商讨，读者证这个类应该至少包括ID，status这两个属性。其中ID应该记录读者证的拥有者以及办理时间的信息，status表示该读者证是否有效。
2. 

===

###Log

===

###Log

===