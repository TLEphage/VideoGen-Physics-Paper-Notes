# --------------------------------------

# **Simulation Prompt #1（现象 1）**

# 2个物体—斜面运动—平面运动—碰撞现象

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* global_friction: 0.15
* time_step: 0.016

**Objects**

* Object A

  * mass: 1.0 kg
  * shape: sphere, radius: 0.1
  * initial_position: (0, 1.0, 0)
  * initial_velocity: (0, 0, 0)
  * friction: 0.12

* Inclined Plane

  * angle: 30°
  * length: 2.0 m

* Flat Plane

  * friction: 0.18

* Object B

  * mass: 1.2 kg
  * shape: cube, size: 0.2
  * initial_position: (2.2, 0.0, 0)
  * initial_velocity: (0, 0, 0)

**Event Timeline**

1. t=0：Object A 在斜面顶部静止。
2. t=0–1.2 s：A 沿斜面无初速度滑下。
3. t≈1.2 s：A 到达平面并以 ~1.5 m/s 继续滑动。
4. t≈1.8 s：A 与 B 发生非完全弹性碰撞（恢复系数 e=0.4）。
5. t>1.8 s：A 减速停止；B 以新速度继续滑动直至停止。

---

# --------------------------------------

# **Simulation Prompt #2（现象 2）**

# 3个物体—平面运动—圆周运动—碰撞现象

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.1

**Objects**

* Object A

  * mass: 0.8 kg
  * shape: sphere
  * initial_position: (0, 0, 0)
  * initial_velocity: (2.0, 0, 0)
  * tether_length: 1.5 m (connected to fixed point at (0,0,0))

* Object B

  * mass: 1.0 kg
  * shape: cube
  * initial_position: (1.5, 0, 0)
  * initial_velocity: (0, 0, 0)

* Object C

  * mass: 0.9 kg
  * shape: sphere
  * initial_position: (2.5, 0, 0)
  * initial_velocity: (0, 0, 0)

**Timeline**

1. A 绕固定点做半径 1.5 m 的圆周运动。
2. 转过约 180° 后，与静止的 B 碰撞（恢复系数 e=0.3）。
3. B 受撞击获得匀减速运动，移动 1 m 后与 C 碰撞。
4. C 获得小速度继续滑行，直到摩擦使其停止。

---

# --------------------------------------

# **Simulation Prompt #3（现象 3）**

# 自由落体—碰撞—反弹平面运动

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.2

**Objects**

* Object A

  * mass: 0.5 kg
  * shape: sphere
  * initial_position: (0, 2.0, 0)
  * initial_velocity: (0, 0, 0)

**Timeline**

1. A 从高度 2 m 自由落体。
2. 落地后与平面发生弹性或半弹性碰撞（e=0.6）。
3. 反弹后落回地面，以速度 ~1.2 m/s 向前滚动。
4. 摩擦逐渐让其停下。

---

# --------------------------------------

# **Simulation Prompt #4（现象 4）**

# 抛射运动—圆周运动物体—多物体碰撞

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)

**Objects**

* Object A（抛射体）

  * mass: 0.4 kg
  * initial_position: (0, 0.5, 0)
  * initial_velocity: (3.5, 2.0, 0)

* Object B（圆周运动）

  * mass: 1.0 kg
  * tether_length: 1.0 m
  * initial_position: (2.0, 0, 0)
  * initial_velocity: circular motion tangent at 1.5 m/s

* Object C

  * mass: 1.2 kg
  * initial_position: (3.0, 0, 0)

**Timeline**

1. A 做抛射运动。
2. 到达某点与做圆周运动的 B 正面碰撞。
3. B 被击出圆周路径，飞向 C。
4. B 与 C 发生第二次碰撞。

---

# --------------------------------------

# **Simulation Prompt #5（现象 5）**

# 推拉运动—斜面运动—物体自转

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.2
* incline_angle: 25°

**Objects**

* Object A（被推的物体）

  * mass: 0.9 kg
  * shape: cylinder
  * initial_position: (0, 0, 0)
  * push_force: (5.0, 0, 0)

**Timeline**

1. A 在平面上被推力加速到 ~2 m/s。
2. A 上斜面并因摩擦产生自转（初始 ω≈2 rad/s）。
3. A 在斜面顶端减速并滑下返回。

---

# --------------------------------------

# **Simulation Prompt #6（现象 6）**

# 浮力—下沉物体碰撞—水面运动

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* fluid_density: 1000 kg/m³

**Objects**

* Object A（漂浮物）

  * density: 600 kg/m³
  * initial_position: (0, 0, 0)

* Object B（下沉物）

  * density: 2000 kg/m³
  * initial_position: (-0.5, 0.5, 0)
  * initial_velocity: (1.0, -0.2, 0)

**Timeline**

1. B 向下运动并从侧面撞击 A。
2. A 被撞后向右滑动 0.5~1 m。
3. B 继续下沉。

---

# --------------------------------------

# **Simulation Prompt #7（现象 7）**

# 圆周运动—绳断—自由落体—碰撞

# --------------------------------------

**Objects**

* Object A

  * mass: 0.6 kg
  * tether_length: 1.2 m
  * circular_speed: 2.5 m/s

* Object B

  * mass: 1.0 kg
  * initial_position: (1.5, 0, 0)

**Timeline**

1. A 做圆周运动。
2. t ≈ 1.6 s：绳断，A 以切线方向飞出。
3. A 落地后撞向 B。

---

# --------------------------------------

# **Simulation Prompt #8（现象 8）**

# 弹簧简谐运动—反弹—第二次抛射

# --------------------------------------

**Objects**

* Object A

  * mass: 0.5 kg
  * spring_k: 80 N/m
  * initial_displacement: 0.1 m

* Barrier

  * fixed_position: (0.5, 0, 0)

**Timeline**

1. A 做简谐运动。
2. 速度最大点撞击挡板。
3. 碰撞后以速度 ~1.8 m/s 被抛射出去。

---

# --------------------------------------

# **Simulation Prompt #9（现象 9）**

# 自转物体—碰撞改变角速度

# --------------------------------------

**Objects**

* Object A

  * mass: 1.0 kg
  * initial_angular_velocity: 5 rad/s
  * initial_linear_velocity: (1.0, 0, 0)

* Object B

  * mass: 1.5 kg
  * initial_angular_velocity: -3 rad/s

**Timeline**

1. A 滚动并自转。
2. 与 B 碰撞。
3. 碰撞后两者角速度发生改变（通过弹性/非弹性模型）。

---

# --------------------------------------

# **Simulation Prompt #10（现象 10）**

# 单摆—绳断—落地碰撞

# --------------------------------------

**Objects**

* Pendulum Bob A

  * mass: 0.8 kg
  * string_length: 1.0 m
  * initial_angle: 35°

* Object B

  * mass: 1.2 kg
  * initial_position: (1.2, 0, 0)

**Timeline**

1. A 做单摆运动。
2. 绳子在最高点断裂。
3. A 进入自由落体并落地。
4. A 继续滑行撞击 B。

---

# --------------------------------------

# **Simulation Prompt #11（现象 11）**

# 平面运动—弹簧简谐运动—碰撞现象

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.12
* time_step: 0.01

**Objects**

* Object A

  * mass: 0.9 kg
  * shape: sphere, r=0.08 m
  * initial_position: (-1.2, 0, 0)
  * initial_velocity: (3.0, 0, 0)
  * friction: 0.12

* WallSpring

  * spring_k: 120 N/m
  * damping: 2.0
  * rest_position: (0.5, 0, 0)

* Object B

  * mass: 0.8 kg
  * shape: cube, size=0.12
  * initial_position: (-0.2, 0, 0)
  * initial_velocity: (0, 0, 0)

**Timeline**

1. t=0：A 以 3.0 m/s 沿 +x 方向移动并撞击 WallSpring，压缩并做简谐振动。
2. A 在反弹途中向 -x 方向返回并在 x≈-0.2 m 处与静止的 B 发生弹性碰撞（e=0.85）。
3. 监测 A 与 B 的位移与速度直至两者静止（由摩擦耗散）。

---

# --------------------------------------

# **Simulation Prompt #12（现象 12）**

# 抛射运动—平面落地—自转（获得角速度）

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.25
* time_step: 0.01

**Objects**

* Projectile A

  * mass: 0.6 kg
  * shape: cylinder (r=0.06, h=0.1)
  * initial_position: (0, 0.5, 0)
  * initial_velocity: (4.0, 3.0, 0)  # v0, θ ≈ 36.9°

* Ground Plane

  * friction: 0.25
  * restitution: 0.4

**Timeline**

1. A 做抛射运动并在落地瞬间与粗糙地面发生碰撞，摩擦矩使其开始自转（赋予角速度 ω≈6 rad/s）。
2. A 在地面以翻滚/滚动混合运动前进并逐步减速直至停止。

---

# --------------------------------------

# **Simulation Prompt #13（现象 13）**

# 绳约束圆周—断绳切线出射—碰撞链

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.1
* time_step: 0.01

**Objects**

* Object A (tethered)

  * mass: 0.7 kg
  * shape: sphere, r=0.07
  * tether_anchor: (0,0,0)
  * tether_length: 1.5 m
  * initial_angular_speed: 2.2 rad/s

* Object B

  * mass: 1.0 kg
  * shape: cube, size=0.15
  * initial_position: (1.6, 0, 0)

* Object C

  * mass: 0.9 kg
  * shape: sphere, r=0.06
  * initial_position: (2.4, 0, 0)

**Timeline**

1. A 做圆周运动；t≈1.4 s 时释放（断绳），A 以切线速度 v = ω·r 飞出。
2. A 在地面与 B 碰撞（e=0.5），B 被推向 C 并与 C 发生第二次碰撞，形成链式反应。

---

# --------------------------------------

# **Simulation Prompt #14（现象 14）**

# 浮力碰撞—自由落体入水—漂浮物推动

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* fluid_density: 1000 kg/m³
* water_surface_y: 0.0
* drag_coefficient: 0.9

**Objects**

* Object A (floating)

  * mass: 0.4 kg
  * volume: 0.0006 m³ (density 667 kg/m³)
  * initial_position: (0.2, 0.0, 0)

* Object B (dropper)

  * mass: 0.8 kg
  * shape: sphere, r=0.07
  * initial_position: (-0.5, 1.5, 0)
  * initial_velocity: (0.5, 0, 0)

**Timeline**

1. B 从 y=1.5 m 自由落体进入水面，溅起水并将 A 推开。
2. A 获得水平速度 ~0.6–1.0 m/s，在水面被拖拽滑动若干距离（受水阻与浮力影响）。
3. B 下沉至底部或继续沉降（取决于其密度设置）。

---

# --------------------------------------

# **Simulation Prompt #15（现象 15）**

# 推力进入圆轨道—出轨平面运动

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.15

**Objects**

* Object A

  * mass: 1.0 kg
  * shape: sphere, r=0.08
  * initial_position: (-2.0, 0, 0)
  * push_force: (8.0, 0, 0) applied from t=0 to t=0.4 s

* Circular Track

  * radius: 1.0 m
  * entry_point: (0.0, 0, 0)
  * track_friction: 0.08

**Timeline**

1. A 被推力加速，经由入口进入圆形轨道并开始约束圆周运动。
2. 在轨道内行进数周，因摩擦或外扰在出口处以速度 v_out 离开轨道并进入平面直线运动直至停止。

---

# --------------------------------------

# **Simulation Prompt #16（现象 16）**

# 斜面撞摆—摆动二次碰撞

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* incline_angle: 28°
* plane_friction: 0.14

**Objects**

* Object A

  * mass: 0.7 kg
  * shape: block, size=(0.15,0.08,0.15)
  * initial_position: (-1.5, 0.8, 0)  # 在斜面上方
  * initial_velocity: (0, 0, 0)

* Pendulum B

  * mass: 0.6 kg
  * string_length: 0.9 m
  * pivot_position: (0.6, 1.0, 0)
  * rest_angle: 0°

**Timeline**

1. A 自斜面滑下并在底端撞击静止摆球 B，B 获得初速度并开始摆动。
2. B 在回摆过程中（靠近垂直方向）与仍未完全静止的 A 发生第二次轻微碰撞。

---

# --------------------------------------

# **Simulation Prompt #17（现象 17）**

# 非线性摆断绳—落地平移

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.16

**Objects**

* Pendulum A

  * mass: 0.9 kg
  * string_length: 1.2 m
  * initial_angle: 70°  # 大角度非线性摆

* Ground Plane

  * friction: 0.16

**Timeline**

1. A 从初角 70° 释放摆动；在最高点或回摆某瞬间触发断绳事件（t 任意）。
2. A 在断绳点转为自由落体并落到地面上，接触后以线速度 v≈1.5 m/s 滚动/滑动并逐渐停止。

---

# --------------------------------------

# **Simulation Prompt #18（现象 18）**

# 自转体碰撞链—角动量传递

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.12

**Objects**

* Object A

  * mass: 1.2 kg
  * shape: disk, r=0.12, thickness=0.02
  * initial_linear_velocity: (1.2, 0, 0)
  * initial_angular_velocity: 8 rad/s

* Object B

  * mass: 0.9 kg
  * shape: disk, r=0.10
  * initial_position: (1.6, 0, 0)
  * initial_angular_velocity: 0 rad/s

* Object C

  * mass: 0.8 kg
  * shape: cube, size=0.12
  * initial_position: (2.6, 0, 0)

**Timeline**

1. A 具有自转与平移并撞击 B，使 B 获得角动量与线动量。
2. B 再向前撞击 C，引起 C 的平移和可能的转动。
3. 记录每一碰撞后的角速度与线速度变化（角动量守恒视摩擦/碰撞模型而定）。

---

# --------------------------------------

# **Simulation Prompt #19（现象 19）**

# 弹簧振子脱离—上斜碰撞

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.15

**Objects**

* Object A (spring-mounted)

  * mass: 0.5 kg
  * spring_k: 100 N/m
  * initial_displacement: -0.12 m
  * position: (-0.8, 0, 0)

* Incline

  * angle: 22°
  * top_position: (0.8, 0.0, 0)

* Object B

  * mass: 0.7 kg
  * position_on_incline: (0.5, 0.05, 0)

**Timeline**

1. A 在弹簧上作简谐运动，于速度峰值处脱离弹簧并以 v≈1.6 m/s 向右移动并登上斜面。
2. A 沿斜面上滑并在中段与 B 发生碰撞（e=0.6），可观察能量分配与动量交换。

---

# --------------------------------------

# **Simulation Prompt #20（现象 20）**

# 抛射入水—浮力/下沉转换

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* fluid_density: 1000 kg/m³
* drag_coefficient: 1.0

**Objects**

* Object A

  * mass: 0.95 kg
  * volume: 0.0008 m³  # 密度 ≈1187.5 kg/m³（略高于水）
  * initial_position: (0, 0.6, 0)
  * initial_velocity: (2.8, 1.8, 0)

**Timeline**

1. A 做抛射并进入水中，因密度稍高于水先短暂下沉。
2. 在水中受浮力与阻力作用，下沉速度减小并在某深度处减速至静止或缓慢上浮（视阻力/附加力设定）。
3. 若设置带有可压缩空气腔/浮力变化，可模拟上浮过程并最终脱出水面。

---

继续 **第 3 批（#21–#30）**，每条依然是可直接用于 Unity / Unreal / MuJoCo / Bullet / PyBullet / Blender Physics 的 **结构化物理仿真 Prompt**。

---

# --------------------------------------

# **Simulation Prompt #21（现象 21）**

# 圆周运动—摩擦衰减—脱轨抛射

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* track_friction: 0.10
* plane_friction: 0.14
* time_step: 0.01

**Objects**

* Object A

  * mass: 0.7 kg
  * shape: sphere, r=0.07
  * constrained_radius: 1.0 m
  * initial_angular_speed: 3.2 rad/s
  * center_of_rotation: (0, 0, 0)

* Ground Plane

  * friction: 0.14

**Timeline**

1. A 在圆轨道上做圆周运动，因摩擦导致角速度逐渐减小。
2. 当角速度衰减至维持向心力不足时，A 在轨道某点脱离约束。
3. A 以切线方向进入自由抛射运动，落地后继续在地面滑行直至停止。

---

# --------------------------------------

# **Simulation Prompt #22（现象 22）**

# 斜面加速—平面滑动—撞击弹簧

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* incline_angle: 30°
* plane_friction: 0.18

**Objects**

* Object A

  * mass: 1.0 kg
  * shape: cube, size=0.15
  * initial_position: (-1.5, 0.7, 0)
  * initial_velocity: (0, 0, 0)

* WallSpring

  * spring_k: 150 N/m
  * damping: 3.0
  * rest_position: (1.0, 0, 0)

**Timeline**

1. A 在斜面上无初速度滑下，到达平面时速度约 v ≈ 2.7 m/s。
2. 在平面继续滑动，受到摩擦减速。
3. 在 x=1.0 m 处撞击弹簧并触发压缩振动，记录最大压缩量与返回速度。

---

# --------------------------------------

# **Simulation Prompt #23（现象 23）**

# 下落穿过液体—阻尼过渡—撞击底部物体

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* fluid_surface_y: 0.8
* fluid_density: 1000 kg/m³
* drag_coefficient: 0.7

**Objects**

* Object A

  * mass: 0.6 kg
  * volume: 0.00045 m³  # density 1333 kg/m³（可下沉）
  * initial_position: (0, 1.5, 0)

* Object B（底部）

  * mass: 1.5 kg
  * shape: block size=0.2
  * initial_position: (0, 0, 0)

**Timeline**

1. A 从 1.5 m 自由落体至水面，在通过水面瞬间受到巨大阻力并显著减速。
2. A 在液体中继续下沉并逐渐趋于 terminal velocity。
3. A 最终撞击底部的 B。
4. 碰撞后 B 获得小位移或轻微滑移。

---

# --------------------------------------

# **Simulation Prompt #24（现象 24）**

# 多级碰撞：推动—反弹—撞击第三物体

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* friction: 0.16

**Objects**

* Object A

  * mass: 0.9 kg
  * initial_velocity: (2.0, 0, 0)
  * shape: sphere r=0.08

* Object B

  * mass: 1.0 kg
  * initial_position: (1.0, 0, 0)

* Object C

  * mass: 1.2 kg
  * initial_position: (2.2, 0, 0)

**Timeline**

1. A 以 2 m/s 撞击 B，产生部分弹性碰撞（e=0.6）。
2. B 被推向 C 并与 C 发生第二次碰撞。
3. 记录每一次碰撞后的速度分布（体现一维动量守恒 + 能量损失）。

---

# --------------------------------------

# **Simulation Prompt #25（现象 25）**

# 单摆击球—球滚动—斜面上滑

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.14
* incline_angle: 20°

**Objects**

* Pendulum A

  * mass: 0.7 kg
  * string_length: 1.0 m
  * initial_angle: 40°

* Object B

  * mass: 0.6 kg
  * shape: sphere r=0.07
  * position: (0.9, 0, 0)

* Incline Plane（B 会滑上去）

  * start_position: (1.1, 0, 0)

**Timeline**

1. A 被释放并摆动，撞击静止的 B。
2. B 获得速度滚动向前。
3. B 上斜面并因重力逐渐减速，在最高点短暂停止后返回。

---

# --------------------------------------

# **Simulation Prompt #26（现象 26）**

# 水中浮体被推—撞击沉体—反弹向上

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* fluid_density: 1000 kg/m³
* drag_coefficient: 0.8

**Objects**

* Floating Object A

  * mass: 0.3 kg
  * volume: 0.0006 m³  # density = 500 kg/m³
  * initial_position: (0, 0, 0)

* Heavy Object B

  * mass: 1.2 kg
  * volume: 0.0007 m³  # density = 1714 kg/m³（下沉）
  * initial_position: (0.5, -0.3, 0)

**Timeline**

1. A 受到水平推力向右加速。
2. 在水中与 B 碰撞后反弹。
3. 浮力驱使 A 向上浮，再次穿出水面。

---

# --------------------------------------

# **Simulation Prompt #27（现象 27）**

# 压缩弹簧发射—飞行—击中目标

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)

**Objects**

* Spring Launcher

  * spring_k: 200 N/m
  * initial_compression: 0.12 m

* Projectile A

  * mass: 0.4 kg
  * shape: sphere r=0.05
  * initial_position: (0, 0.1, 0)

* Target B

  * mass: 1.0 kg
  * initial_position: (2.5, 0, 0)

**Timeline**

1. 弹簧释放，给予 A 初速度 v = sqrt(kx²/m)。
2. A 做抛射运动飞向目标。
3. 与 B 发生碰撞，B 获得部分动量，A 反弹或滑落。

---

# --------------------------------------

# **Simulation Prompt #28（现象 28）**

# 旋转物体落地—摩擦力产生滚动

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* friction: 0.18

**Objects**

* Object A

  * mass: 0.8 kg
  * shape: cylinder r=0.1
  * initial_position: (0, 1.2, 0)
  * initial_angular_velocity: 10 rad/s
  * initial_linear_velocity: (0, 0, 0)

**Timeline**

1. A 自由落体落地。
2. 碰撞瞬间因初始自转与摩擦耦合，A 获得向前的滚动速度。
3. 最终进入纯滚动并因摩擦缓慢停止。

---

# --------------------------------------

# **Simulation Prompt #29（现象 29）**

# 推力加速—撞击摆锤—摆锤反向击回

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.15

**Objects**

* Object A

  * mass: 1.0 kg
  * initial_velocity: (2.5, 0, 0)

* Pendulum B

  * mass: 0.6 kg
  * string_length: 1.0 m
  * anchor: (1.0, 1.2, 0)

**Timeline**

1. A 以 2.5 m/s 撞击静止摆锤 B。
2. B 被击动，摆向右侧达到最大位移。
3. 回摆时，B 再次与 A 发生轻微二次碰撞（取决于 A 是否仍在附近）。

---

# --------------------------------------

# **Simulation Prompt #30（现象 30）**

# 斜面下滑—平面加速—二次跃起（跳台效应）

# --------------------------------------

**Environment**

* gravity: (0, -9.8, 0)
* plane_friction: 0.12
* incline_angle: 35°

**Objects**

* Object A

  * mass: 0.9 kg
  * shape: sphere r=0.09
  * initial_position: (-1.4, 0.9, 0)

* Small Ramp (jump ramp)

  * position: (1.0, 0, 0)
  * angle: 20°

**Timeline**

1. A 在斜面上滑下并进入平面。
2. 继续滑动一段后登上小跳台并被抛射至空中。
3. A 落地后继续滑动，最终停下。

---