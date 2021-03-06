#List Problems In Requirement
===

###Problem1 用“方便”、“等”、“详细信息”这些词语描述需求
1. “读者能够方便办读书证”，“方便挂失补办等”，“修改个人登录密码等”，“方便准确查询自己已经借阅的书籍”，“以及想要借阅的书籍的详细信息”
2. “操作方便快捷易于理解”
3. “查询读者信息、书籍信息、借阅记录等”
4. “如借书限额、借书期限、书籍逾期不还的处罚额度等”

###Solution
通过采访和后续交流的方式问清需求。有很多需求双方都不是很清楚，需要在建模的过程中才能发现，并与客户核实。

===

###Problem2 需求描述不统一，甚至冲突
1. 读者提的“读书证”的概念，前台提的“借书证”的概念，两者功能相似，怀疑指的是同一个东西
2. 采访中，对于违约金的收取，前台代表认为“只接受现金”，财务代表认为“现金，网上支付，第三方支付都可”
3. 新书录入功能的职责归属，在原始需求文档中，这个职责归属前台人员，但是采访中，却更改为维护人员

###Solution
1. 后经核实，两者确实是同一个东西，所以在文档中统一称作“读者证”
2. 后经核实，以财务代表的陈述为准
3. 将职责归属为维护人员，并做相应的修改

===

###Problem3 细节陈述缺失
1. 业务流程细节缺失：办理读者证流程，借书还书以及预约的流程，挂失的流程
2. 重要参数缺失：违约金计算公式
3. 实体功能陈述缺失：自助终端的功能陈述
4. 用况陈述缺失：缺失图书又重新找回

###Solution
1. 首先根据经验设计一种通常的流程，然后再向客户代表进行确认，有冲突的地方再作修改
2. 采访时提问
3. 对终端的功能记录：“扫书，接受预约金”，并没有说明是录入书籍信息还是借还书籍，预约金是来预约什么的，，之后通过邮件询问后，补充了该部分：“扫书来进行借还书，挂失读者证，预约书籍，接受办卡（读者证）预约金，识别读者证，分发读者证”
4. 这个问题是在进行需求建模的过程中发现的，随后向客户进行确认，应该是不接受已经标记为缺失的书籍

===

###Problem4 最初的设计可行性有问题
最初设计的类图中没有读者证这个类，所以在处理挂失请求的时候，无法辨别同一个人过去办理的读者证和新办理的读者证的区别，因此挂失服务无法完成。

###Solution
增加一个读者证类，封装了两个属性，一是status用来表示当前该读者证有效性的信息；二是ID能够表示该读者证的拥有者以及办理时间的信息