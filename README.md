# -
不知火无2019

灭火机器人

底层相关驱动已经封装好,此工程仅为逻辑控制部分，该部分将由组员共同完成。

车身资源:
红外光电传感器* 5:   连接的IO口名称为:LIG1-LIG5(从左至右)
声音传感器* 1:       连接的IO口名称为MI
火焰传感器* 5:       FIR1-FIR5(从左至右)
寻白线传感器* 1:     TRA
如何读取传感器状态:   直接读IO口的高低电平
例if(MI==0)

Turn_x(unsigned char Dir,unsigned char Speed) //Dir为运行方向:STRA前进 LEFT左转 RIGHT右转 BACK后退 默认速度Speed=60;
方向控制由该函数完成,该函数由定时器中断调用(每1ms进一次中断),在main函数中只需改变Dir
例Dir=STRA;(STRA等为宏定义)

2019.9.5



