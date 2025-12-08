## 个人总结


### 物理现象

这篇论文的**Morpheus基准**共设计了9类核心物理实验，对应不同的物理现象，各现象的具体设定及物理参数如下：

1. 下落（Falling）

**物理现象**：物体从静止状态下落至接触地面，验证匀重力加速度与能量守恒规律。
**物理参数**
- 变量维度：2个（物体类型、释放高度）
- 具体参数：
  1. 物体类型：乒乓球、白板笔、胶带卷、苹果；
  2. 释放高度：不同垂直高度（机械执行器控制乒乓球释放高度，其余物体为手动释放的多组高度）；
  3. 运动约束：仅受重力（忽略空气阻力），垂直方向加速度为$g$（重力加速度），水平方向速度$v_x=0$。

2. 抛射运动（Projectile motion）

**物理现象**：小球以不同初速度、角度发射，验证动量守恒、能量守恒及重力场均匀性。
**物理参数**
- 变量维度：3个（发射角度、弹力大小、小球颜色）
- 具体参数：
  1. 发射装置：3D打印弹弓式发射器（橡胶绳提供弹力）；
  2. 发射角度：多组可调倾斜角度；
  3. 发射弹力：3档橡胶绳拉伸程度（对应不同初速度）；
  4. 小球属性：同材质不同颜色的3种塑料小球；
  5. 运动约束：水平方向动量$p_x=mv_x$守恒，垂直方向加速度为$g$，轨迹符合抛物线规律。

3. 滚动（Rolling）

**物理现象**：物体沿斜面滚落，验证能量守恒及滚动动力学规律。
**物理参数**

- 变量维度：2个（斜面倾角、物体类型）
- 具体参数：
  1. 物体类型：密封满罐、空罐、橙子；
  2. 斜面倾角：多组可调坡度；
  3. 运动约束：存在滚动摩擦，满足平动与转动的耦合动力学，总机械能（平动动能+转动动能+重力势能）近似守恒。

4. 滑动（Sliding）

**物理现象**：书本沿斜面滑动，验证能量守恒及滑动摩擦力作用规律。
**物理参数**
- 变量维度：1个（斜面倾角）
- 具体参数：
  1. 滑动对象：平板书本；
  2. 斜面倾角：多组可调坡度；
  3. 运动约束：仅存在平动（无转动），受重力分力与滑动摩擦力，加速度$a$由斜面倾角$\theta$和摩擦系数$\mu$决定（$a = g\sin\theta - \mu g\cos\theta$）。

5. 完整约束摆（Holonomic pendulum）

**物理现象**：刚性杆连接小球做周期性摆动，验证能量守恒与简谐运动规律。
**物理参数**
- 变量维度：1个（初始摆角）
- 具体参数：
  1. 摆结构：金属刚性杆+末端乒乓球（质心与杆末端同轴）；
  2. 初始摆角：以竖直静止为$0^\circ$，设置多组初始偏转角度；
  3. 运动约束：摆长$l$固定，小角度下满足简谐运动（周期$T=2\pi\sqrt{l/g}$），总机械能$E=\frac{1}{2}ml^2\dot{\theta}^2 + mgl(1-\cos\theta)$近似守恒（忽略阻尼）。

6. 双摆（Double pendulum）

**物理现象**：两级摆锤的混沌运动，验证非线性动力学系统的守恒规律。
**物理参数**
- 变量维度：1个（上层摆锤初始高度）
- 具体参数：
  1. 摆结构：木质底座+金属杆+两级3D打印摆锤（紫色上段、橙色下段）；
  2. 初始状态：以上层摆锤的初始竖直高度为变量；
  3. 运动约束：两级摆长固定，总机械能守恒（忽略阻尼），运动呈现混沌特性。

7. 弹跳（Bouncing）

**物理现象**：小球接触地面后的回弹运动，验证重力加速度与弹跳过程的能量守恒。
**物理参数**
- 变量维度：1个（下落初始高度）
- 具体参数：
  1. 实验对象：乒乓球；
  2. 初始条件：不同下落高度（决定首次撞击地面的速度）；
  3. 运动约束：每次弹跳后机械能因碰撞损耗而衰减，无弹跳阶段加速度为$g$，水平方向速度$v_x$守恒。

8. 碰撞（Collision）

**物理现象**：不同质量小球的碰撞过程，验证动量守恒与能量守恒（弹性碰撞假设）。
**物理参数**
- 变量维度：3个（碰撞物体质量、初始速度、物体尺寸）
- 具体参数：
  1. 碰撞组合：大球撞小球、等质量球互撞、小球撞大球；
  2. 初始状态：一侧小球静止，另一侧小球以随机初速度（手动轻推）撞击；
  3. 约束条件：假设为弹性碰撞，总动量$m_1v_{10}+m_2v_{20}=m_1v_1+m_2v_2$与总动能$\frac{1}{2}m_1v_{10}^2+\frac{1}{2}m_2v_{20}^2=\frac{1}{2}m_1v_1^2+\frac{1}{2}m_2v_2^2$守恒。

9. 弹簧（Spring）

**物理现象**：弹簧悬挂重物的简谐振动，验证胡克定律与振动周期守恒。
**物理参数**
- 变量维度：1个（初始位移/冲量）
- 具体参数：
  1. 实验装置：竖直弹簧+圆柱形金属配重；
  2. 初始条件：手动施加的不同初始位移/冲量（决定振动振幅）；
  3. 运动约束：满足胡克定律$F=-kx$，小阻尼下振动周期$T=2\pi\sqrt{m/k}$（$k$为弹簧劲度系数，$m$为配重质量），机械能（弹性势能+重力势能+动能）近似守恒。



### Prompt

1. 运动类型：Falling Ball（自由下落）
- **Base Prompt**：Orange ping-pong ball falling down and making impact with the table surface below. Fixed camera view, no camera movement.
- **Enhanced Prompt**：A ping-pong ball is captured in mid-air, suspended above a laboratory table, poised to make contact with the surface below. The ball’s descent is governed by the force of gravity, creating an arc that suggests a controlled experiment in progress. The backdrop is a stark, clinical room with a neutral palette, punctuated by the sterile lines of a metal frame and the functional design of a nearby cabinet. The lighting is subdued, casting a soft glow that highlights the ball’s trajectory and the anticipation of impact. The table beneath the ball is marked with faint lines, perhaps indicating measurements or guidelines for the experiment. As the ball continues its downward journey, it will likely bounce off the table, adding a dynamic element to the scene and marking the conclusion of this controlled descent. Fixed camera view, no camera movement.

2. 运动类型：Projectile（抛射运动）
- **Base Prompt**：A single, small 3D-printed ball, dark gray in color, is launched from a plastic, small-scale ramp with a slight upward angle. The ball follows a natural, smooth, arcing trajectory upward and then downward, continuing along that arc until it exits the right side of the video frame. The video should accurately simulate the ball’s motion under standard earth gravity, showing a clear parabolic arc. The video should emphasize a smooth and realistic physics-based movement of the ball without any sudden changes in speed. The ball should not bounce or collide with any objects in the scene. Fixed camera view, no camera movement.
- **Enhanced Prompt**：In a meticulously crafted scene, a solitary, dark gray 3D-printed ball, with its sleek, spherical form, is propelled from a plastic ramp that slopes gently upward. The ball, weighing a mere fraction of a kilogram, is captured in high-definition, showcasing every nuance of its motion. As it leaves the ramp’s edge, the ball arcs gracefully into the air, its trajectory a perfect parabola that mirrors the laws of physics under standard earth gravity. The video’s frame follows the ball’s smooth ascent and descent, highlighting the ball’s consistent speed and the absence of any sudden accelerations or decelerations. The scene remains unobstructed, ensuring that the ball’s journey is uninterrupted by any external forces, save for the pull of gravity, resulting in a visually stunning and scientifically accurate demonstration of a parabolic motion. Fixed camera view, no camera movement.

3. 运动类型：Rolling Can（斜面滚动）
- **Base Prompt**：An empty soda can rolls down a wooden surface. Experiment carried out in a laboratory controlled environment. Fixed camera view, no camera movement.
- **Enhanced Prompt**：An empty aluminum red soda can rolls steadily down an inclined wooden board in a controlled laboratory environment. This motion should be depicted with physical realism, accurately simulating the key dynamics: the can accelerates under gravity, with its combined rotational and translational movement appearing authentic and governed by the frictional interaction with the wooden surface, ensuring a physically plausible rolling movement. Fixed camera view, no camera movement.

4. 运动类型：Sliding Book（斜面滑动）
- **Base Prompt**：A book slides down a wooden surface. Experiment carried out in a laboratory controlled environment. Fixed camera view, no camera movement.
- **Enhanced Prompt**：A book slides steadily down an inclined wooden board in a controlled laboratory environment. This motion should be depicted with physical realism, accurately simulating the key dynamics: the book accelerates due to the component of gravity acting along the incline, opposed by kinetic friction from the wooden surface. Its movement should be purely translational, maintaining consistent contact with the board and without any significant rotation or tumbling, ensuring a physically plausible descent. Fixed camera view, no camera movement.

5. 运动类型：Holonomic Pendulum（完整约束单摆）
- **Base Prompt**：A single pendulum moving retrogressively back and forth. At the bottom of a pendulum, there is a ball attached to it. The pendulum is holonomic. Fixed camera view, no camera movement.
- **Enhanced Prompt**：A pendulum with a spherical ball attached swings back and forth in a controlled manner, its motion captured in a moment of retrograde swing. The pendulum’s arm, likely made of metal, extends horizontally from a stand, connected to a pivot point that allows for rotational movement. The ball, positioned at the lower end of the pendulum, appears to be in motion, indicating the pendulum’s swing. The environment suggests a laboratory or testing setting, with a backdrop of technical apparatus and equipment, and the lighting is artificial, casting a uniform glow over the scene. The pendulum’s movement, while currently in a retrogressive swing, could potentially change direction, continuing its oscillatory motion. Fixed camera view, no camera movement.

6. 运动类型：Double Pendulum（双摆）
- **Base Prompt**：Double pendulum, consisting of a purple and an orange segment. Each segment moves independently. Fixed camera view, no camera movement.
- **Enhanced Prompt**：In a meticulously arranged laboratory setting, a double pendulum setup swings gracefully, each pendulum segment adhering to the immutable laws of physics. The upper pendulum, a sleek purple rod, contrasts strikingly with the lower orange rod, both suspended from a sturdy, metallic frame. The room is bathed in soft, ambient light, casting subtle shadows that accentuate the pendulums’ arcs. The scene captures the intricate dance of the pendulums, their movements a mesmerizing testament to the natural order, with each swing a silent symphony of motion and balance. Fixed camera view, no camera movement.

7. 运动类型：Bouncing Ball（弹跳运动）
- **Base Prompt**：A single orange ping pong ball bounces vertically as a result of making impact with the table after being in free fall. The ball starts in the center of the frame, and moves upwards. Fixed camera view, no camera movement.
- **Enhanced Prompt**：A solitary orange ping pong ball, with its vibrant hue standing out against the stark white of the table, plummets from the center of the frame. As the ball bounces upwards, it arcs gracefully, the trajectory a perfect parabola. The frame remains centered, emphasizing the ball’s solitary dance of motion and the physics of its rebound. Fixed camera view, no camera movement.

8. 运动类型：Collision（碰撞运动）
- **Base Prompt**：Generate a realistic video of two metallic spheres colliding. In the first frames the leftmost sphere in the video is moving towards the static one. At the moment of contact the ball in motion transfer its kinetic energy to the ball at rest. The two spheres have identical physical properties, namely material, shapes, masses. The momentum should be conserved. Fixed camera view, no camera movement.
- **Enhanced Prompt**：In a high-definition, slow-motion sequence, two identical metallic spheres, each polished to a mirror-like finish, are meticulously positioned on a frictionless surface. The left sphere, propelled by an unseen force, hurtles towards the stationary sphere, its trajectory a perfect parabola. As the oncoming sphere approaches, the static sphere begins to subtly vibrate, a prelude to the impending collision. The moment of contact is captured in stunning detail, revealing the transfer of kinetic energy as the moving sphere’s momentum is transferred to the stationary one. The spheres, crafted from the same dense material, maintain their spherical shapes and masses, ensuring the conservation of momentum throughout the impact. The scene is illuminated by a single, soft light source, casting long shadows and emphasizing the physics of the collision. Fixed camera view, no camera movement.

9. 运动类型：Spring（弹簧简谐振动）
- **Base Prompt**：A single metallic slotted mass attached on a spring moving periodically up and down. Fixed camera view, no camera movement.
- **Enhanced Prompt**：In a meticulously crafted scene, a solitary metallic slotted mass, polished to a gleaming silver, is ingeniously attached to a tensioned spring. The mass, weighing several pounds, oscillates with a fluid grace, its movement initiated by the subtle release of the spring. The camera captures the mass as it arcs upwards, the tension in the spring visible, before it gently descends with a rhythmic sway, the sound of its metallic slats clinking softly in the background. The scene is set against a stark white backdrop, emphasizing the stark contrast between the mass and the spring, and the smooth, periodic motion of the mechanical dance. Fixed camera view, no camera movement.

