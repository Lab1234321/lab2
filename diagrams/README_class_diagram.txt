1、类图中一共有九个类，分别为Book、ManageSystem、LentHistory（借阅历史）、Reader、Maintainer(维护人员)、Receptionist（前台）、Finance（财务人员）、User、LibraryCard。
2、ManageSystem维护Reader和Book的两个列表，表示当前所有的读者和图书馆中所有书籍，另外系统还需要维护违约金的处罚参数和当前日期（以便计算是否应该提醒还书，用户需要支付多少违约金等）；系统还具有一些重要功能，如：处理办证请求，处理借书、预约请求，计算违约金，催还等。
3、User作为另外三个类的父类主要有两个属性：UserID 和 password以及登录方法。
4、LibiaryCard包含读书证的ID和此读书证所有者的ID以及此证当前的状态（已被挂失？可以正常使用？）