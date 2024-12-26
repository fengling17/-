# 项目说明
- 1、前端页面扫雷，无接口数据。
- 2、index1.html为鼠标扫雷，index2.html为坐标扫雷。两种实现方式，数据结构不同，底层原理是一样的：数据驱动，将变化用页面展示。
# 技术栈
- Vue2+JS
# 项目运行
- Alt+B
# 模型构建
    //构建思路：
    //一、点击开始游戏按钮，获取游戏区域大小，并初始化游戏区域

    //    1、给开始按钮绑定点击事件，将inpa赋值给gamesize
    //    2、监听gamesize变化，对其数据处理生成坐标点集合area
    //    3、通过area数据渲染游戏区域
    //    4、以小于area20%的量生成地雷集合bombs，设置安全区safety
    //    5、给每个cent节点添加动态样式，以计算属性监听每个坐标 (bomb=>c3,safety=>c2,else=>c1)


    //二、点击扫雷按钮，获取扫雷点坐标，并判断是否安全，并渲染结果

    //    1、给开始按钮绑定点击事件，对输入数据X、Y各减 1 后赋值给point
    //    2、判断point是否在bombs集合中。
    //          如果在,则bomb被赋值，触发计算属性，cent样式变为c3
    //          如果不在，则point被添加到safety中。触发计算属性，cent样式变为c2


    //三、游戏结束，游戏重开

    //    1、游戏结束条件：bomb有值=>success || safety.length === area.length - bombs.length => fail
    //    2、游戏重开：给开始按钮的点击事件继续丰富，data初始化


    //四、宏观处理、流程优化、细节丰富

    //    1、flag:true =>禁止开始按钮 || flag:false => 禁用扫雷按钮
    //    2、输入框限制输入格式:输入框数据的两个正则、inpb重复输入限制(以上两点没做，增加代码可读性,格子1*1有问题，根炸弹数量有关，只用于演示原理，所以不加规则)
# 演示视频
- 坐标扫雷
https://github.com/user-attachments/assets/d126f1e3-ad1b-4daa-ad69-9dc02cba0e34

- 鼠标扫雷
https://github.com/user-attachments/assets/db24d0f5-0c63-456c-8846-a97c76929e46





