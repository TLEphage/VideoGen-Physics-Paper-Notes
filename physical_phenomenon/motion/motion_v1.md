# 基础物理现象汇总

全局可调节变量：

1. 摄像机位置和角度
2. 物体类型（形状）：球体/正方体/圆柱体/长方体/保龄球/橡胶球/乒乓球/小轿车/公交车/飞机/木材/水果/鸡蛋/笔/胶带卷
3. 物体材料：铁/木/橡胶/塑料/玻璃/陶瓷/铝/钢/泡沫
4. 物体质量 $m \in [0.1, 1000.0]$
5. 物体位置、颜色、尺寸、**个数**
6. 接触面材质：光滑木板/抛光金属/冰面/玻璃/塑胶跑道/沥青/沙地/水泥/泥土/雪地/湿滑路面/塑料/地毯
7. 重力加速度 $g$

生成物体：先随机得到物体个数，对于每个物体再独立设置初值



## 平面运动

> 连续运动 

**物理量：**

1. 运动方向 $direction = (x_0, y_0, z_0)$
2. 运动初速度 $v_0 \in [0,100]$

3. 摩擦因数：$\mu \in [0,1)$​
4. 牵引力：$F \in [0,100000]$​
5. 加速度：$a \in [-100,100]$​
6. 运动方式：滑动/滚动



相关运动：

匀速直线运动

匀加速直线运动

匀减速直线运动

3D远近运动



## 斜面运动

> 连续运动

**物理量：**

1. 斜面倾角 $\theta \in (0,90)$​
2. 运动方向 $direction = (x_0, y_0, z_0)$
3. 运动初速度 $v_0 \in [0,100]$​
4. 摩擦因数：$\mu \in [0,1)$​
5. 牵引力：$F \in [0,100000]$​
6. 加速度：$a \in [-100,100]$​
7. 距离平面高度：$h \in (0,100]$​
8. 运动方式：滑动/滚动



相关运动：

斜面滚动

斜面滑动

岩石滚山坡现象



## 自由落体运动

> 连续运动

**物理量：**

1. 释放高度 $h \in (0,100]$



相关运动：

自由下落

橡胶球的自由下落与弹性碰撞运动

下落物体弹性碰撞反弹现象

苹果落地碰撞破碎现象

材料硬度现象（鸡蛋撞岩石破碎）

## 抛射运动

> 连续运动

**物理量：**

1. 发射角度 $\theta \in (-90,90)$
2. 运动方向 $direction = (x_0, y_0, z_0)$
3. 运动初速度 $v_0 \in [0,100]$



相关运动：

抛射运动

带转动的抛射运动



## 碰撞现象

> 非连续运动

物理量：

1. 物体A碰撞前运动方向 $d_A = (x_A,y_A,z_A)$
2. 物体A碰撞前速度 $v_A \in [0,100]$​
3. 物体A碰撞后运动方向 $d_A' = (x_A',y_A',z_A')$
4. 物体A碰撞后速度 $v_A' \in [-100,100]$​
5. 碰撞恢复系数 $e \in [0,1]$
6. 碰撞类型：物体碰物体/物体碰平面
7. 物体A碰撞前运动方向 $d_B = (x_B,y_B,z_B)$
8. 物体B碰撞前速度 $v_B \in [-100,100]$​
9. 物体A碰撞后运动方向 $d_B' = (x_B',y_B',z_B')$
10. 物体B碰撞后速度 $v_B' \in [-100,100]$​



相关运动：

橡胶球的自由下落与弹性碰撞运动

下落物体弹性碰撞反弹现象

两球碰撞现象

木球与铁立方的碰撞运动

苹果落地碰撞破碎现象

材料硬度现象（鸡蛋撞岩石破碎）

刚体拖动碰撞现象

多米诺骨牌受阻现象



## 推拉现象

> 连续运动

物理量：

1. 外力大小 $F \in [0,100000]$
2. 外力方向 $direction = (x_1, y_1, z_1)$
3. 外力作用点 $point = (x_2,y_2,z_2)$



相关运动：

刚体拖动碰撞现象

白板笔的书写运动



## 浮力现象

>连续运动

物理量：

1. 运动方向 $direction = (x_0, y_0, z_0)$
2. 运动初速度 $v_0 \in [0,100]$
3. 物体密度 $\rho_{obj} \in [500, 10000]$
4. 液体类型：水/油/酒精/盐水
5. 液体密度 $\rho_{fluid} \in [1000, 2000]$​
6. 下落高度 $h \in [0,100]$



相关运动：

浮力现象（铁沉水）

木块的水上漂浮运动



## 物体自转

>连续运动

物理量：

1. 角速度 $\omega \in (0, 10\pi]$​
2. 角加速度 $\alpha \in [-2\pi, 2\pi]$​
3. 阻尼系数 $\gamma$



相关运动：

斜面滚动

带转动的抛射运动

岩石滚山坡现象



## 圆周运动

>连续运动

**物理量：**

1. 角速度 $\omega \in (0, 10\pi]$​
2. 运动半径 $r \in [0,100]$
3. 径向力 $F_r \in [0,100000]$
4. 切向力 $F_t \in [0,100000]$
5. 运动中心 $center = (x_1, y_1, z_1)$
6. 牵引绳端点位置 $endpoint = (x_2, y_2, z_2)$



相关运动：

圆周轨道运动现象

定轴转动现象



## 简谐运动(弹簧)

>连续运动

物理量：

1. 初始位移$x_0 \in [0,100]$​
2. 运动方向 $direction = (x_0, y_0, z_0)$
3. 运动初速度 $v_0 \in [0,100]$​
4. 劲度系数 $k \in [10,1000]$
5. 阻尼系数$\gamma$



相关运动：

弹簧振子往复振动现象

阻尼振动现象



## 简谐运动(单摆)

>连续运动

物理量：

1. 运动初速度 $v_0 \in [0,100]$
2. 初始摆角 $\theta_0 \in [0,90]$
3. 摆长 $l \in (0,100]$
4. 阻尼系数$\gamma$



相关运动：

单摆往复摆动现象



## 非线性摆运动

> 连续运动

物理量：

1. 上段摆初始高度 $h \in [0,100]$
2. 两段摆长 $l_1,l_2 \in [0,100]$
3. 阻尼系数$\gamma$



相关运动：

双摆混沌摆动现象



# 混合运动现象汇总

1. 2个物体 - 斜面运动-平面运动-碰撞现象  
- **description:**  
  物体A从斜面滑下，滑到平面上做匀减速直线运动，与静止的物体B发生碰撞，碰撞后物体B开始运动，物体A反弹或静止。  
  *(An object A slides down an inclined plane, then moves on a flat surface with uniform deceleration, collides with a stationary object B, after which object B starts moving and object A rebounds or stops.)*

2. 1个物体 - 自由落体-碰撞现象-平面运动  
- **description:**  
  物体从高处自由落体，撞击地面后反弹（弹性碰撞），然后在地面上滚动一段距离后停止。  
  *(An object falls freely from a height, rebounds after hitting the ground (elastic collision), then rolls on the ground for a distance before stopping.)*

3. 2个物体 - 抛射运动-碰撞现象-自由落体  
- **description:**  
  物体A以一定角度被抛出，在空中与物体B发生碰撞，碰撞后两物体分别以不同轨迹自由落体。  
  *(Object A is projected at an angle, collides with object B in mid-air, after which both objects fall freely along different trajectories.)*

4. 1个物体 - 推拉现象-平面运动-斜面运动  
- **description:**  
  物体在平面上被推动，加速运动后滑上斜面，在斜面上减速至停止，然后反向滑下。  
  *(An object is pushed on a flat surface, accelerates, then slides up an inclined plane, decelerates to a stop, and then slides back down.)*

5. 2个物体 - 浮力现象-碰撞现象-平面运动  
- **description:**  
  木块在水中漂浮，被另一个下沉的铁块撞击后，木块在水面上滑动，铁块沉底。  
  *(A wooden block floats on water, is hit by a sinking iron block, causing the wood to slide on the water surface while the iron sinks to the bottom.)*

6. 1个物体 - 物体自转-抛射运动-自由落体  
- **description:**  
  一个旋转的球被抛出，在空中旋转着做抛体运动，然后以自由落体方式落地。  
  *(A spinning ball is thrown, moves as a projectile while rotating in mid-air, and then falls freely to the ground.)*

7. 1个物体 - 圆周运动-物体自转-平面运动  
- **description:**  
  物体在圆周轨道上做匀速圆周运动，同时自转，后脱离轨道在平面上滑动至停止。  
  *(An object moves in uniform circular motion along a circular track while spinning, then detaches and slides on a flat surface until it stops.)*

8. 1个物体 - 简谐运动(弹簧)-碰撞现象  
- **description:**  
  弹簧振子做简谐振动，撞击到另一物体后停止振动，被撞物体开始运动。  
  *(A spring oscillator undergoes simple harmonic motion, collides with another object, stops vibrating, and the struck object starts moving.)*

9. 1个物体 - 简谐运动(单摆)-碰撞现象  
- **description:**  
  单摆做摆动，摆球撞击静止物体后，摆球反弹，被撞物体开始运动。  
  *(A pendulum swings, its bob collides with a stationary object, the bob rebounds, and the struck object starts moving.)*

10. 2个物体 - 斜面运动-碰撞现象-自由落体-平面运动  
- **description:**  
  物体A从斜面滑下，撞击物体B，使物体B飞出并自由落体，物体A继续在平面上滑动。  
  *(Object A slides down an incline, collides with object B, causing object B to fly out and fall freely, while object A continues sliding on a flat surface.)*

11. 1个物体 - 推拉现象-圆周运动-物体自转  
- **description:**  
  物体被绳子牵引做圆周运动，同时自转，后绳子断裂，物体因惯性做直线运动。  
  *(An object is pulled by a rope to undergo circular motion while spinning, then the rope breaks, and the object continues in a straight line due to inertia.)*

12. 2个物体 - 自由落体-碰撞现象-斜面运动  
- **description:**  
  两物体从不同高度自由落体，先后撞击斜面，沿斜面滚动或滑动至平面。  
  *(Two objects fall freely from different heights, hit an inclined plane successively, and then roll or slide down to a flat surface.)*

13. 1个物体 - 浮力现象-物体自转-平面运动  
- **description:**  
  一个旋转的物体被投入水中，上浮至水面后继续旋转，并在水面上滑动。  
  *(A spinning object is dropped into water, floats to the surface while spinning, and then slides on the water surface.)*

14. 2个物体 - 抛射运动-碰撞现象-斜面运动-平面运动  
- **description:**  
  物体A被抛出，在空中撞击物体B，两物体分别落在斜面和平面上，并继续运动。  
  *(Object A is projected, collides with object B in mid-air, and the two objects land on an inclined plane and a flat surface respectively, continuing to move.)*

15. 1个物体 - 简谐运动(弹簧)-推拉现象  
- **description:**  
  弹簧振子被外力推拉后做简谐振动，外力撤去后继续振动直至停止。  
  *(A spring oscillator is pushed/pulled by an external force, then undergoes simple harmonic motion after the force is removed, until it stops.)*

16. 2个物体 - 圆周运动-碰撞现象-自由落体  
- **description:**  
  两物体在圆周轨道上运动并相撞，飞出轨道后做自由落体运动。  
  *(Two objects move on a circular track and collide, then fly off the track and fall freely.)*

17. 1个物体 - 物体自转-斜面运动-平面运动-碰撞现象  
- **description:**  
  一个旋转的球从斜面滚下，在平面上滚动并撞击墙壁后反弹。  
  *(A spinning ball rolls down an inclined plane, rolls on a flat surface, and rebounds after hitting a wall.)*

18. 2个物体 - 自由落体-浮力现象-碰撞现象  
- **description:**  
  木块和铁块同时自由落体入水，木块上浮，铁块下沉，两者在水中相撞。  
  *(A wooden block and an iron block fall freely into water simultaneously, the wood floats up, the iron sinks, and they collide in the water.)*

19. 1个物体 - 抛射运动-物体自转-自由落体-碰撞现象  
- **description:**  
  一个旋转的物体被抛出，做抛体运动后自由落体，撞击地面后反弹。  
  *(A spinning object is thrown, follows a projectile motion, then falls freely, and rebounds after hitting the ground.)*

20. 2个物体 - 推拉现象-平面运动-碰撞现象-斜面运动  
- **description:**  
  物体A被推动在平面上运动，撞击物体B，两物体一起滑上斜面后减速停止。  
  *(Object A is pushed to move on a flat surface, collides with object B, and both slide up an inclined plane before decelerating to a stop.)*

21. 1个物体 - 圆周运动-简谐运动(弹簧)  
- **description:**  
  物体做圆周运动时通过弹簧与中心连接，同时做简谐振动。  
  *(An object moves in a circle while connected to the center by a spring, simultaneously undergoing simple harmonic motion.)*

22. 2个物体 - 斜面运动-自由落体-碰撞现象-平面运动  
- **description:**  
  物体A从斜面滑下后自由落体，撞击地面上的物体B，两物体在平面上滑动。  
  *(Object A slides down an incline, falls freely, hits object B on the ground, and both slide on a flat surface.)*

23. 1个物体 - 浮力现象-推拉现象-平面运动  
- **description:**  
  物体在水中被推拉做加速运动，后浮出水面，在水面上继续滑动。  
  *(An object is pushed/pulled in water to accelerate, then floats to the surface and continues sliding on the water.)*

24. 2个物体 - 物体自转-碰撞现象-抛射运动  
- **description:**  
  两个旋转的物体相撞，碰撞后分别以抛射运动飞向不同方向。  
  *(Two spinning objects collide, and after the collision, they are projected in different directions.)*

25. 1个物体 - 简谐运动(单摆)-自由落体  
- **description:**  
  单摆摆动过程中摆绳断裂，摆球做自由落体运动。  
  *(During the swing of a pendulum, the string breaks, and the bob falls freely.)*

26. 2个物体 - 平面运动-碰撞现象-圆周运动  
- **description:**  
  两物体在平面上做直线运动并相撞，碰撞后一物体进入圆周轨道运动。  
  *(Two objects move in straight lines on a flat surface and collide, after which one object enters circular motion on a track.)*

27. 1个物体 - 推拉现象-物体自转-斜面运动-平面运动  
- **description:**  
  物体被推动在平面上旋转前进，后滑上斜面，再滑回平面停止。  
  *(An object is pushed to rotate while moving on a flat surface, then slides up an incline, and slides back to the flat surface to stop.)*

28. 2个物体 - 自由落体-碰撞现象-浮力现象  
- **description:**  
  两物体先后自由落体入水，在水中相撞后，一物体上浮，一物体下沉。  
  *(Two objects fall freely into water successively, collide underwater, after which one floats up and the other sinks.)*

29. 1个物体 - 抛射运动-碰撞现象-物体自转-平面运动  
- **description:**  
  物体被抛出后撞击墙面，反弹并旋转，后在平面上滚动至停止。  
  *(An object is thrown, hits a wall, rebounds while spinning, and then rolls on a flat surface until it stops.)*

30. 2个物体 - 斜面运动-碰撞现象-推拉现象-平面运动  
- **description:**  
  物体A从斜面滑下撞击物体B，随后物体B被外力拉动在平面上运动。  
  *(Object A slides down an incline and collides with object B, then object B is pulled by an external force to move on a flat surface.)*

31. 1个物体 - 圆周运动-物体自转-碰撞现象-自由落体  
- **description:**  
  物体在圆周轨道上旋转运动，脱离轨道后撞击另一物体，两物体一起自由落体。  
  *(An object rotates on a circular track, detaches, collides with another object, and both fall freely together.)*

32. 2个物体 - 浮力现象-推拉现象-碰撞现象-平面运动  
- **description:**  
  水中两物体被推拉相互靠近并相撞，碰撞后一物体浮出水面并在水面滑动。  
  *(Two objects in water are pushed/pulled toward each other and collide, after which one floats to the surface and slides on the water.)*

33. 1个物体 - 简谐运动(弹簧)-碰撞现象-斜面运动  
- **description:**  
  弹簧振子振动时撞击斜面，沿斜面滑动一段距离后停止。  
  *(A spring oscillator vibrates, hits an inclined plane, slides along the incline for a distance, and stops.)*

34. 2个物体 - 平面运动-碰撞现象-物体自转-抛射运动  
- **description:**  
  两物体在平面上滑动相撞，碰撞后两物体旋转着被抛向空中。  
  *(Two objects slide on a flat surface and collide, after which both are thrown into the air while spinning.)*

35. 1个物体 - 推拉现象-圆周运动-简谐运动(弹簧)  
- **description:**  
  物体被牵引做圆周运动，同时通过弹簧与中心连接做简谐振动。  
  *(An object is pulled in circular motion while connected to the center by a spring, undergoing simple harmonic motion simultaneously.)*

36. 2个物体 - 自由落体-斜面运动-碰撞现象-平面运动  
- **description:**  
  物体A自由落体至斜面，沿斜面滑下后撞击平面上的物体B。  
  *(Object A falls freely onto an inclined plane, slides down, and collides with object B on a flat surface.)*

37. 1个物体 - 物体自转-浮力现象-推拉现象  
- **description:**  
  旋转的物体被投入水中，受浮力上浮，同时被外力推拉移动。  
  *(A spinning object is dropped into water, floats up due to buoyancy, and is simultaneously pushed/pulled by an external force.)*

38. 2个物体 - 抛射运动-碰撞现象-自由落体-斜面运动  
- **description:**  
  物体A被抛出后与物体B相撞，两物体分别自由落体至斜面和平面。  
  *(Object A is projected and collides with object B, after which both fall freely onto an inclined plane and a flat surface respectively.)*

39. 1个物体 - 简谐运动(单摆)-碰撞现象-平面运动  
- **description:**  
  单摆摆动时撞击另一物体，摆球反弹，被撞物体在平面上滑动。  
  *(A pendulum swings and hits another object, the bob rebounds, and the struck object slides on a flat surface.)*

40. 2个物体 - 圆周运动-碰撞现象-物体自转-平面运动  
- **description:**  
  两物体在圆周轨道上运动并相撞，碰撞后脱离轨道，旋转着在平面上滑动。  
  *(Two objects move on a circular track and collide, then detach from the track and slide on a flat surface while spinning.)*

41. 1个物体 - 推拉现象-平面运动-碰撞现象-自由落体  
- **description:**  
  物体被推动在平面上加速，撞击障碍物后弹起并自由落体。  
  *(An object is pushed to accelerate on a flat surface, hits an obstacle, bounces up, and falls freely.)*

42. 2个物体 - 浮力现象-碰撞现象-物体自转-平面运动  
- **description:**  
  水中两旋转物体相撞，一物体浮出水面并在水面旋转滑动。  
  *(Two spinning objects collide in water, one floats to the surface and rotates while sliding on the water.)*

43. 1个物体 - 斜面运动-物体自转-碰撞现象-抛射运动  
- **description:**  
  旋转物体从斜面滚下，撞击挡板后以抛射运动飞出。  
  *(A spinning object rolls down an incline, hits a barrier, and is projected into the air.)*

44. 2个物体 - 自由落体-碰撞现象-推拉现象-平面运动  
- **description:**  
  两物体自由落体至平面，碰撞后一物体被外力拉动在平面上运动。  
  *(Two objects fall freely onto a flat surface, collide, and one is pulled by an external force to move on the surface.)*

45. 1个物体 - 圆周运动-简谐运动(单摆)  
- **description:**  
  单摆的摆球在水平面内做圆周运动，同时做摆动。  
  *(The bob of a pendulum moves in a horizontal circle while also swinging.)*

46. 2个物体 - 抛射运动-碰撞现象-浮力现象  
- **description:**  
  两物体被抛入水中，在水中相撞后，一物体上浮，一物体下沉。  
  *(Two objects are thrown into water, collide underwater, after which one floats up and the other sinks.)*

47. 1个物体 - 推拉现象-物体自转-圆周运动  
- **description:**  
  物体被推拉做直线运动的同时旋转，后进入圆周轨道运动。  
  *(An object is pushed/pulled in a straight line while spinning, then enters circular motion on a track.)*

48. 2个物体 - 斜面运动-碰撞现象-自由落体-浮力现象  
- **description:**  
  物体A从斜面滑下后自由落体入水，与水中物体B相撞。  
  *(Object A slides down an incline, falls freely into water, and collides with object B in the water.)*

49. 1个物体 - 简谐运动(弹簧)-碰撞现象-物体自转  
- **description:**  
  弹簧振子振动时撞击一旋转物体，使其改变转速和方向。  
  *(A spring oscillator vibrates and hits a spinning object, changing its rotation speed and direction.)*

50. 2个物体 - 平面运动-碰撞现象-抛射运动-自由落体  
- **description:**  
  两物体在平面上相撞，碰撞后一物体被抛向空中做自由落体。  
  *(Two objects collide on a flat surface, after which one is thrown into the air and falls freely.)*

51. 1个物体 - 浮力现象-推拉现象-物体自转-平面运动  
- **description:**  
  旋转物体在水中被推拉做加速运动，浮出水面后在水面旋转滑动。  
  *(A spinning object is pushed/pulled in water to accelerate, floats to the surface, and rotates while sliding on the water.)*

52. 2个物体 - 圆周运动-碰撞现象-斜面运动  
- **description:**  
  两物体在圆周轨道上运动并相撞，碰撞后一物体飞向斜面并滑下。  
  *(Two objects move on a circular track and collide, after which one flies onto an inclined plane and slides down.)*

53. 1个物体 - 推拉现象-平面运动-斜面运动-碰撞现象  
- **description:**  
  物体被推动在平面上运动，滑上斜面后与斜面顶端物体相撞。  
  *(An object is pushed to move on a flat surface, slides up an incline, and collides with an object at the top of the incline.)*

54. 2个物体 - 自由落体-碰撞现象-物体自转-平面运动  
- **description:**  
  两物体自由落体至平面，碰撞后旋转着在平面上滑动。  
  *(Two objects fall freely onto a flat surface, collide, and then slide on the surface while spinning.)*

55. 1个物体 - 抛射运动-物体自转-碰撞现象-斜面运动  
- **description:**  
  旋转物体被抛出，撞击斜面后沿斜面滑动。  
  *(A spinning object is thrown, hits an inclined plane, and slides along the incline.)*

56. 2个物体 - 浮力现象-碰撞现象-推拉现象-平面运动  
- **description:**  
  水中两物体相撞，碰撞后一物体被推拉至水面并在水面滑动。  
  *(Two objects collide in water, after which one is pushed/pulled to the water surface and slides on it.)*

57. 1个物体 - 简谐运动(单摆)-碰撞现象-自由落体  
- **description:**  
  单摆摆动时撞击另一物体，摆球反弹后自由落体。  
  *(A pendulum swings and hits another object, the bob rebounds and falls freely.)*

58. 2个物体 - 斜面运动-碰撞现象-圆周运动  
- **description:**  
  物体A从斜面滑下撞击物体B，使物体B进入圆周轨道运动。  
  *(Object A slides down an incline and collides with object B, causing object B to enter circular motion on a track.)*

59. 1个物体 - 推拉现象-物体自转-自由落体-碰撞现象  
- **description:**  
  旋转物体被推动后自由落体，撞击地面后反弹。  
  *(A spinning object is pushed, then falls freely, and rebounds after hitting the ground.)*

60. 2个物体 - 平面运动-碰撞现象-浮力现象  
- **description:**  
  两物体在平面上相撞后飞入水中，一物体漂浮，一物体下沉。  
  *(Two objects collide on a flat surface and fly into water, one floats and the other sinks.)*

61. 1个物体 - 圆周运动-物体自转-碰撞现象-斜面运动  
- **description:**  
  物体在圆周轨道上旋转运动，脱离后撞击斜面并滑下。  
  *(An object rotates on a circular track, detaches, hits an inclined plane, and slides down.)*

62. 2个物体 - 自由落体-碰撞现象-推拉现象-斜面运动  
- **description:**  
  两物体自由落体至斜面，碰撞后一物体被推拉沿斜面运动。  
  *(Two objects fall freely onto an inclined plane, collide, and one is pushed/pulled to move along the incline.)*

63. 1个物体 - 浮力现象-物体自转-碰撞现象-平面运动  
- **description:**  
  旋转物体在水中上浮，与另一物体相撞，后在水面滑动。  
  *(A spinning object floats up in water, collides with another object, and then slides on the water surface.)*

64. 2个物体 - 抛射运动-碰撞现象-物体自转-自由落体  
- **description:**  
  两旋转物体被抛出并在空中相撞，碰撞后分别自由落体。  
  *(Two spinning objects are thrown and collide in mid-air, after which both fall freely.)*

65. 1个物体 - 简谐运动(弹簧)-推拉现象-碰撞现象  
- **description:**  
  弹簧振子被推拉后振动，撞击另一物体后停止振动。  
  *(A spring oscillator is pushed/pulled and vibrates, then stops vibrating after hitting another object.)*

66. 2个物体 - 平面运动-碰撞现象-圆周运动-物体自转  
- **description:**  
  两物体在平面上相撞，碰撞后一物体旋转着进入圆周轨道。  
  *(Two objects collide on a flat surface, after which one enters circular motion on a track while spinning.)*

67. 1个物体 - 推拉现象-斜面运动-自由落体-碰撞现象  
- **description:**  
  物体被推上斜面后自由落体，撞击地面后反弹。  
  *(An object is pushed up an incline, then falls freely, and rebounds after hitting the ground.)*

68. 2个物体 - 浮力现象-碰撞现象-斜面运动-平面运动  
- **description:**  
  水中两物体相撞，一物体滑上斜面，另一物体在水面滑动。  
  *(Two objects collide in water, one slides up an inclined plane, and the other slides on the water surface.)*

69. 1个物体 - 物体自转-抛射运动-碰撞现象-自由落体  
- **description:**  
  旋转物体被抛出，在空中撞击另一物体后自由落体。  
  *(A spinning object is thrown, collides with another object in mid-air, and then falls freely.)*

70. 2个物体 - 圆周运动-碰撞现象-自由落体-斜面运动  
- **description:**  
  两物体在圆周轨道上相撞后飞出，自由落体至斜面并滑下。  
  *(Two objects collide on a circular track and fly off, fall freely onto an inclined plane, and slide down.)*

71. 1个物体 - 简谐运动(单摆)-碰撞现象-斜面运动  
- **description:**  
  单摆摆动时撞击斜面，沿斜面滑动一段距离后停止。  
  *(A pendulum swings and hits an inclined plane, slides along the incline for a distance, and stops.)*

72. 2个物体 - 平面运动-碰撞现象-推拉现象-物体自转  
- **description:**  
  两物体在平面上相撞，碰撞后一物体被推拉并旋转。  
  *(Two objects collide on a flat surface, after which one is pushed/pulled and spins.)*

73. 1个物体 - 浮力现象-推拉现象-碰撞现象-自由落体  
- **description:**  
  物体在水中被推拉，与另一物体相撞后飞出水面并自由落体。  
  *(An object is pushed/pulled in water, collides with another object, flies out of the water, and falls freely.)*

74. 2个物体 - 自由落体-碰撞现象-圆周运动  
- **description:**  
  两物体自由落体至圆周轨道并相撞，后沿轨道运动。  
  *(Two objects fall freely onto a circular track and collide, then move along the track.)*

75. 1个物体 - 抛射运动-物体自转-碰撞现象-平面运动  
- **description:**  
  旋转物体被抛出，撞击地面后反弹并在平面上滚动。  
  *(A spinning object is thrown, hits the ground, rebounds, and rolls on a flat surface.)*

76. 2个物体 - 斜面运动-碰撞现象-浮力现象  
- **description:**  
  物体从斜面滑下后冲入水中，与水中物体相撞。  
  *(An object slides down an incline and rushes into water, colliding with an object in the water.)*

77. 1个物体 - 推拉现象-圆周运动-碰撞现象-自由落体  
- **description:**  
  物体被牵引做圆周运动，绳子断裂后飞出，自由落体至地面。  
  *(An object is pulled in circular motion, the rope breaks, it flies off, and falls freely to the ground.)*

78. 2个物体 - 平面运动-碰撞现象-物体自转-抛射运动  
- **description:**  
  两物体在平面上滑动相撞，碰撞后旋转着被抛向空中。  
  *(Two objects slide on a flat surface and collide, after which both are thrown into the air while spinning.)*

79. 1个物体 - 简谐运动(弹簧)-碰撞现象-物体自转  
- **description:**  
  弹簧振子振动时撞击一静止旋转物体，使其开始运动。  
  *(A spring oscillator vibrates and hits a stationary spinning object, causing it to start moving.)*

80. 2个物体 - 浮力现象-碰撞现象-推拉现象-斜面运动  
- **description:**  
  水中两物体相撞，碰撞后一物体被推拉上斜面。  
  *(Two objects collide in water, after which one is pushed/pulled up an inclined plane.)*

81. 1个物体 - 物体自转-自由落体-碰撞现象-平面运动  
- **description:**  
  旋转物体自由落体，撞击地面后反弹并在平面上滚动。  
  *(A spinning object falls freely, hits the ground, rebounds, and rolls on a flat surface.)*

82. 2个物体 - 圆周运动-碰撞现象-抛射运动  
- **description:**  
  两物体在圆周轨道上相撞后飞出，做抛射运动。  
  *(Two objects collide on a circular track and fly off, following projectile motion.)*

83. 1个物体 - 推拉现象-平面运动-碰撞现象-物体自转  
- **description:**  
  物体被推动在平面上运动，撞击另一物体后开始旋转。  
  *(An object is pushed to move on a flat surface, collides with another object, and starts spinning.)*

84. 2个物体 - 自由落体-碰撞现象-推拉现象-浮力现象  
- **description:**  
  两物体自由落体入水，碰撞后一物体被推拉至水面。  
  *(Two objects fall freely into water, collide, and one is pushed/pulled to the water surface.)*

85. 1个物体 - 斜面运动-物体自转-碰撞现象-圆周运动  
- **description:**  
  旋转物体从斜面滚下，撞击后进入圆周轨道运动。  
  *(A spinning object rolls down an incline, collides, and enters circular motion on a track.)*

86. 2个物体 - 抛射运动-碰撞现象-斜面运动-平面运动  
- **description:**  
  两物体被抛出并在空中相撞，分别落在斜面和平面上并继续运动。  
  *(Two objects are thrown and collide in mid-air, land on an inclined plane and a flat surface respectively, and continue moving.)*

87. 1个物体 - 浮力现象-物体自转-推拉现象-碰撞现象  
- **description:**  
  旋转物体在水中被推拉，与另一物体相撞后改变运动状态。  
  *(A spinning object is pushed/pulled in water, collides with another object, and changes its motion state.)*

88. 2个物体 - 平面运动-碰撞现象-自由落体-斜面运动  
- **description:**  
  两物体在平面上相撞，一物体弹起后自由落体至斜面并滑下。  
  *(Two objects collide on a flat surface, one bounces up, falls freely onto an inclined plane, and slides down.)*

89. 1个物体 - 简谐运动(单摆)-碰撞现象-抛射运动  
- **description:**  
  单摆摆动时撞击一物体，使其以抛射运动飞出。  
  *(A pendulum swings and hits an object, causing it to be projected into the air.)*

90. 2个物体 - 圆周运动-碰撞现象-物体自转-自由落体  
- **description:**  
  两旋转物体在圆周轨道上相撞后飞出，自由落体至地面。  
  *(Two spinning objects collide on a circular track and fly off, falling freely to the ground.)*

91. 1个物体 - 推拉现象-斜面运动-碰撞现象-物体自转  
- **description:**  
  物体被推上斜面，与斜面顶端物体相撞后旋转着滑下。  
  *(An object is pushed up an incline, collides with an object at the top, and slides down while spinning.)*

92. 2个物体 - 自由落体-碰撞现象-圆周运动-物体自转  
- **description:**  
  两物体自由落体至圆周轨道并相撞，后旋转着沿轨道运动。  
  *(Two objects fall freely onto a circular track and collide, then move along the track while spinning.)*

93. 1个物体 - 浮力现象-碰撞现象-平面运动-推拉现象  
- **description:**  
  物体在水中与另一物体相撞后浮出水面，被推拉在水面滑动。  
  *(An object collides with another in water, floats to the surface, and is pushed/pulled to slide on the water.)*

94. 2个物体 - 抛射运动-碰撞现象-自由落体-浮力现象  
- **description:**  
  两物体被抛入水中，在水中相撞后一物体上浮，一物体下沉。  
  *(Two objects are thrown into water, collide underwater, after which one floats up and the other sinks.)*

95. 1个物体 - 物体自转-圆周运动-碰撞现象-斜面运动  
- **description:**  
  旋转物体在圆周轨道上运动，脱离后撞击斜面并滑下。  
  *(A spinning object moves on a circular track, detaches, hits an inclined plane, and slides down.)*

96. 2个物体 - 平面运动-碰撞现象-推拉现象-自由落体  
- **description:**  
  两物体在平面上相撞，碰撞后一物体被推拉并自由落体。  
  *(Two objects collide on a flat surface, after which one is pushed/pulled and falls freely.)*

97. 1个物体 - 简谐运动(弹簧)-碰撞现象-自由落体  
- **description:**  
  弹簧振子振动时撞击一物体，使其自由落体。  
  *(A spring oscillator vibrates and hits an object, causing it to fall freely.)*

98. 2个物体 - 斜面运动-碰撞现象-物体自转-抛射运动  
- **description:**  
  物体从斜面滑下撞击另一物体，碰撞后两物体旋转着被抛向空中。  
  *(An object slides down an incline and collides with another, after which both are thrown into the air while spinning.)*

99. 1个物体 - 推拉现象-浮力现象-碰撞现象-平面运动  
- **description:**  
  物体在水中被推拉，与另一物体相撞后浮出水面并在水面滑动。  
  *(An object is pushed/pulled in water, collides with another object, floats to the surface, and slides on the water.)*

100. 2个物体 - 圆周运动-碰撞现象-斜面运动-平面运动  
- **description:**  
  两物体在圆周轨道上相撞后飞出，一物体落在斜面并滑下至平面。  
  *(Two objects collide on a circular track and fly off, one lands on an inclined plane and slides down to a flat surface.)*
