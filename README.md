# AiVirtualMouse
一个基于电脑摄像头手部关键点识别的虚拟鼠标，已做成exe文件，windows系统可直接使用，不用自己配置环境，也不需要GPU  
下载地址为：百度盘：https://pan.baidu.com/s/1nQONI1mIq39Bnff78ML4QA  提取码：yrmy 

双击dist/AiVirtualMouseProject/AiVirtualMouseProject.exe即可运行程序。  
对着弹出的显示框按一下q（小写）可退出程序。  

参考：  
https://www.computervision.zone/courses/ai-virtual-mouse/  

自己的改动：
1.添加了拖拽和滚动中键的功能，所有办公用的鼠标功能需求应该都能满足。  
2.优化了参考视频里鼠标移动的控制方式，由伸出一根食指移动来控制改为用掌心移动来控制，这样在食指进行其他操作时就不会导致鼠标大距离飘移。  
3.优化了参考视频里单击鼠标的控制方式，由检测食指和中指指尖的距离，改为检测食指和中指的下按速率，当食指下按速率大于临界值时单击左键，当中指下按速率大于临界值时单击右键，这样更符合使用鼠标的习惯。这样优化还有一个好处是，原视频检测的指尖距离在屏幕平面的投影会随着手部的转动而发生改变，从而造成误触；而优化后，不管怎么转，由于指尖投影到屏幕平面的y坐标不变，因此并不会因手部的转动而导致误触。
4.拖拽上，在食指按下后，若保持食指不动，则进入拖拽状态，移动手掌即可拖拽目标，再将食指抬起即可解除拖拽状态，这样也更符合日常鼠标使用习惯。
5.为右手鼠标使用者优化了有效控制框的位置和大小，现在使用右手可以在比较舒适的范围内移动来控制鼠标在全屏的移动，而不需要再将右手伸到身体左侧才能控制鼠标抵达屏幕的左侧。

使用方法：  
1.移动鼠标：		  右手五指伸出，移动手掌即可（注意不要移得太快，否则会误触右键和左键）  
2.单击左键：		  右手五指伸出的前提下，像按鼠标左键一样用力按一下食指  
3.单击右键：		  右手五指伸出的前提下，像按鼠标右键一样用力按一下中指  
4.向上滚动中键：	仅伸出食指即可  
5.向下滚动中键：	仅伸出中指即可  
6.拖拽：		      在其他四指伸出的前提下，仅收回食指（令指尖低于根部），稍等片刻，维持食指收回状态，移动手掌即可  
7.解除拖拽：		  在拖拽状态下，将食指返回伸出状态（令指尖高于根部）即可  
8.打开文件：		  先单击右键再在弹出的菜单中的“打开”选项单击左键即可  
