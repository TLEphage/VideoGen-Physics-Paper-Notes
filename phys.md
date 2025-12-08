## 物理现象汇总

### 1. 匀速直线运动现象

- **具体描述**：保龄球、红色橡胶球等物体在光滑平面/木质赛道上保持恒定速度做直线运动
- **物理现象类型**：匀速直线运动
- **运动类型**：连续运动
- **物理参数**：恒定速度、物体类型（保龄球、红色橡胶球）、接触面摩擦系数（近似为0）
- **完整prompt**："A bowling ball moving steadily down a polished wooden lane..."

### 2. 匀加速直线运动现象

- **具体描述**：红色轿车、黑色越野SUV等物体在平直路面上沿直线做匀加速运动
- **物理现象类型**：匀加速直线运动
- **运动类型**：连续运动
- **物理参数**：恒定加速度$a_x$、初始速度、物体类型（红色轿车、黑色越野SUV）、路面摩擦系数
- **完整prompt**："A black off-road SUV accelerating in a straight line on sandy terrain..."

### 3. 匀减速直线运动现象

- **具体描述**：黄色公交车、银色跑车等物体在平直路面上沿直线做匀减速运动
- **物理现象类型**：匀减速直线运动
- **运动类型**：连续运动
- **物理参数**：恒定减速度（$-a_x$）、初始速度、物体类型（黄色公交车、银色跑车）、路面摩擦系数
- **完整prompt**："A silver sports car moves in a straight line on a countryside road at dusk..."

### 4. 3D远近运动现象

- **具体描述**：保龄球、战斗机等物体沿深度方向靠近/远离镜头，伴随尺寸视觉变化
- **物理现象类型**：3D平移运动
- **运动类型**：连续运动
- **物理参数**：深度方向速度、物体初始距离、物体尺寸、重力加速度$g$
- **完整prompt**："A bowling ball moving from the far end of a polished wooden lane toward the camera..."

### 5. 自由下落现象

- **具体描述**：各类物体（乒乓球、白板笔、胶带卷、苹果等）从不同高度由静止释放，仅在重力作用下垂直下落直至接触下方表面
- **物理现象类型**：自由落体运动
- **运动类型**：连续运动
- **物理参数**：释放高度（不同层级）、物体类型（乒乓球、白板笔、胶带卷、苹果）、重力加速度$g$
- **完整prompt**：
  - Base prompt: "Orange ping-pong ball falling down and making impact with the table surface below. Fixed camera view, no camera movement."
  - Enhanced prompt: "A ping-pong ball is captured in mid-air, suspended above a laboratory table, poised to make contact with the surface below. The ball’s descent is governed by the force of gravity, creating an arc that suggests a controlled experiment in progress. The backdrop is a stark, clinical room with a neutral palette, punctuated by the sterile lines of a metal frame and the functional design of a nearby cabinet. The lighting is subdued, casting a soft glow that highlights the ball’s trajectory and the anticipation of impact. The table beneath the ball is marked with faint lines, perhaps indicating measurements or guidelines for the experiment. As the ball continues its downward journey, it will likely bounce off the table, adding a dynamic element to the scene and marking the conclusion of this controlled descent. Fixed camera view, no camera movement."

### 6. 抛射运动现象

- **具体描述**：3D打印小球以不同初始角度和速度被发射，在空中做抛物线运动直至飞出画面
- **物理现象类型**：抛体运动
- **运动类型**：连续运动
- **物理参数**：发射角度、弹弓拉伸程度（对应初始速度）、小球颜色、重力加速度$g$
- **完整prompt**：
  - Base prompt: "A single, small 3D-printed ball, dark gray in color, is launched from a plastic, small-scale ramp with a slight upward angle. The ball follows a natural, smooth, arcing trajectory upward and then downward, continuing along that arc until it exits the right side of the video frame. The video should accurately simulate the ball’s motion under standard earth gravity, showing a clear parabolic arc. The video should emphasize a smooth and realistic physics-based movement of the ball without any sudden changes in speed. The ball should not bounce or collide with any objects in the scene. Fixed camera view, no camera movement."
  - Enhanced prompt: "In a meticulously crafted scene, a solitary, dark gray 3D-printed ball, with its sleek, spherical form, is propelled from a plastic ramp that slopes gently upward. The ball, weighing a mere fraction of a kilogram, is captured in high-definition, showcasing every nuance of its motion. As it leaves the ramp’s edge, the ball arcs gracefully into the air, its trajectory a perfect parabola that mirrors the laws of physics under standard earth gravity. The video’s frame follows the ball’s smooth ascent and descent, highlighting the ball’s consistent speed and the absence of any sudden accelerations or decelerations. The scene remains unobstructed, ensuring that the ball’s journey is uninterrupted by any external forces, save for the pull of gravity, resulting in a visually stunning and scientifically accurate demonstration of a parabolic motion. Fixed camera view, no camera movement."

### 7. 带转动的抛射运动现象

- **具体描述**：画笔/漆刷以一定角度被抛出，在空中做抛物线运动的同时绕自身轴线转动
- **物理现象类型**：复合抛体-转动运动
- **运动类型**：连续运动
- **物理参数**：发射角度、初始平动速度、初始角速度$\omega$、重力加速度$g$
- **完整prompt**："A paintbrush is thrown at an angle, rotating while falling..."

### 8. 橡胶球的自由下落与弹性碰撞运动

- **具体描述**：橡胶球在重力作用下自由下落，接触地面后发生弹性碰撞并反弹，多次反弹后因能量损耗静止
- **物理现象类型**：自由落体+弹性碰撞运动
- **运动连续性**：非连续运动（每次碰撞为间断点）
- **物理参数**：下落高度、重力加速度$g$、弹性恢复系数、空气阻力系数
- **完整prompt**：A rubber ball falls freely under gravity, accelerating as it descends. Upon hitting the ground, it undergoes an elastic collision.

### 9. 斜面滚动现象

- **具体描述**：不同类型物体（满罐、空罐、橙子）从不同倾角的木质斜面顶端释放，沿斜面做滚动运动
- **物理现象类型**：刚体滚动运动
- **运动类型**：连续运动
- **物理参数**：斜面倾角、物体类型（满铝罐、空铝罐、橙子）、重力加速度$g$、摩擦系数（隐含）
- **完整prompt**：
  - Base prompt: "An empty soda can rolls down a wooden surface. Experiment carried out in a laboratory controlled environment. Fixed camera view, no camera movement."
  - Enhanced prompt: "An empty aluminum red soda can rolls steadily down an inclined wooden board in a controlled laboratory environment. This motion should be depicted with physical realism, accurately simulating the key dynamics: the can accelerates under gravity, with its combined rotational and translational movement appearing authentic and governed by the frictional interaction with the wooden surface, ensuring a physically plausible rolling movement. Fixed camera view, no camera movement."

### 10. 斜面滑动现象

- **具体描述**：书本从不同倾角的木质斜面顶端释放，沿斜面做纯平动滑动运动
- **物理现象类型**：质点滑动运动
- **运动类型**：连续运动
- **物理参数**：斜面倾角、物体类型（书本）、重力加速度$g$、滑动摩擦系数（隐含）
- **完整prompt**：
  - Base prompt: "A book slides down a wooden surface. Experiment carried out in a laboratory controlled environment. Fixed camera view, no camera movement."
  - Enhanced prompt: "A book slides steadily down an inclined wooden board in a controlled laboratory environment. This motion should be depicted with physical realism, accurately simulating the key dynamics: the book accelerates due to the component of gravity acting along the incline, opposed by kinetic friction from the wooden surface. Its movement should be purely translational, maintaining consistent contact with the board and without any significant rotation or tumbling, ensuring a physically plausible descent. Fixed camera view, no camera movement."

### 11. 岩石滚山坡现象

- **具体描述**：岩石从陡峭山坡顶端滚落，沿坡面做加速运动并伴随姿态变化
- **物理现象类型**：重力主导的坡面滚动-平动复合运动
- **运动类型**：连续运动
- **物理参数**：山坡倾角、岩石形状与质量、坡面摩擦系数、重力加速度$g$
- **完整prompt**："A rock tumbles down on a steep hillside"

### 12. 弹簧振子往复振动现象

- **具体描述**：金属槽码悬挂于竖直弹簧下端，从平衡位置被拉开后做周期性上下振动
- **物理现象类型**：简谐振动
- **运动类型**：连续运动
- **物理参数**：初始位移（对应初始力）、弹簧劲度系数（隐含）、槽码质量、重力加速度$g$、阻尼系数（隐含）
- **完整prompt**：
  - Base prompt: "A single metallic slotted mass attached on a spring moving periodically up and down. Fixed camera view, no camera movement."
  - Enhanced prompt: "In a meticulously crafted scene, a solitary metallic slotted mass, polished to a gleaming silver, is ingeniously attached to a tensioned spring. The mass, weighing several pounds, oscillates with a fluid grace, its movement initiated by the subtle release of the spring. The camera captures the mass as it arcs upwards, the tension in the spring visible, before it gently descends with a rhythmic sway, the sound of its metallic slats clinking softly in the background. The scene is set against a stark white backdrop, emphasizing the stark contrast between the mass and the spring, and the smooth, periodic motion of the mechanical dance. Fixed camera view, no camera movement."

### 13. 单摆往复摆动现象

- **具体描述**：刚性金属杆末端的乒乓球从不同初始摆角释放，做周期性往复摆动
- **物理现象类型**：简谐摆动（小角度近似）
- **运动类型**：连续运动
- **物理参数**：初始摆角、摆长、重力加速度$g$、阻尼系数（隐含）
- **完整prompt**：
  - Base prompt: "A single pendulum moving retrogressively back and forth. At the bottom of a pendulum, there is a ball attached to it. The pendulum is holonomic. Fixed camera view, no camera movement."
  - Enhanced prompt: "A pendulum with a spherical ball attached swings back and forth in a controlled manner, its motion captured in a moment of retrograde swing. The pendulum’s arm, likely made of metal, extends horizontally from a stand, connected to a pivot point that allows for rotational movement. The ball, positioned at the lower end of the pendulum, appears to be in motion, indicating the pendulum’s swing. The environment suggests a laboratory or testing setting, with a backdrop of technical apparatus and equipment, and the lighting is artificial, casting a uniform glow over the scene. The pendulum’s movement, while currently in a retrogressive swing, could potentially change direction, continuing its oscillatory motion. Fixed camera view, no camera movement."

### 14. 双摆混沌摆动现象

- **具体描述**：双段摆（紫色和橙色摆杆）从不同初始高度释放，做非线性混沌摆动
- **物理现象类型**：非线性摆运动
- **运动类型**：连续运动
- **物理参数**：上段摆初始高度、两段摆长、重力加速度$g$、阻尼系数（隐含）
- **完整prompt**：
  - Base prompt: "Double pendulum, consisting of a purple and an orange segment. Each segment moves independently. Fixed camera view, no camera movement."
  - Enhanced prompt: "In a meticulously arranged laboratory setting, a double pendulum setup swings gracefully, each pendulum segment adhering to the immutable laws of physics. The upper pendulum, a sleek purple rod, contrasts strikingly with the lower orange rod, both suspended from a sturdy, metallic frame. The room is bathed in soft, ambient light, casting subtle shadows that accentuate the pendulums’ arcs. The scene captures the intricate dance of the pendulums, their movements a mesmerizing testament to the natural order, with each swing a silent symphony of motion and balance. Fixed camera view, no camera movement."

### 15. 阻尼振动现象

- **具体描述**：装饰铃铛/单摆受阻尼作用，振幅随时间衰减的摆动
- **物理现象类型**：阻尼简谐振动
- **运动类型**：连续运动
- **物理参数**：初始振幅、阻尼系数、摆长/弹簧劲度系数、重力加速度$g$
- **完整prompt**："A small decorative bell hanging from a fine chain..."

### 16. 圆周轨道运动现象

- **具体描述**：小卫星/彗星绕气态巨行星/恒星做稳定圆周运动
- **物理现象类型**：匀速圆周运动
- **运动类型**：连续运动
- **物理参数**：轨道角速度$\omega$、轨道半径、中心天体与绕行天体质量（隐含）、引力常数（隐含）
- **完整prompt**："A tiny moonlet orbits a gas giant along a smooth, circular path..."

### 17. 定轴转动现象

- **具体描述**：金属杆/木质销钉绕自身轴线做匀速转动
- **物理现象类型**：刚体定轴转动
- **运动类型**：连续运动
- **物理参数**：恒定角速度$\omega$、转动惯量（隐含）、转轴位置
- **完整prompt**："A wooden dowel rotating gently on a tiled kitchen..."

### 18. 下落物体弹性碰撞反弹现象

- **具体描述**：下落物体（如乒乓球）接触地面后发生弹性碰撞，沿原路径向上反弹
- **物理现象类型**：弹性碰撞运动
- **运动类型**：非连续运动（碰撞瞬间运动状态突变）
- **物理参数**：物体释放高度、重力加速度$g$、碰撞恢复系数（隐含）
- **完整prompt**：
  - Base prompt: "A single orange ping pong ball bounces vertically as a result of making impact with the table after being in free fall. The ball starts in the center of the frame, and moves upwards. Fixed camera view, no camera movement."
  - Enhanced prompt: "A solitary orange ping pong ball, with its vibrant hue standing out against the stark white of the table, plummets from the center of the frame. As the ball bounces upwards, it arcs gracefully, the trajectory a perfect parabola. The frame remains centered, emphasizing the ball’s solitary dance of motion and the physics of its rebound. Fixed camera view, no camera movement."

### 19. 两球碰撞现象

- **具体描述**：不同质量的金属球发生碰撞，其中一球初始静止，另一球以一定速度撞击
- **物理现象类型**：刚体碰撞运动
- **运动类型**：非连续运动（碰撞瞬间状态突变）
- **物理参数**：两球质量（等质量/不等质量）、初始撞击速度、重力加速度$g$、碰撞恢复系数（隐含）
- **完整prompt**：
  - Base prompt: "Generate a realistic video of two metallic spheres colliding. In the first frames the leftmost sphere in the video is moving towards the static one. At the moment of contact the ball in motion transfer its kinetic energy to the ball at rest. The two spheres have identical physical properties, namely material, shapes, masses. The momentum should be conserved. Fixed camera view, no camera movement."
  - Enhanced prompt: "In a high-definition, slow-motion sequence, two identical metallic spheres, each polished to a mirror-like finish, are meticulously positioned on a frictionless surface. The left sphere, propelled by an unseen force, hurtles towards the stationary sphere, its trajectory a perfect parabola. As the oncoming sphere approaches, the static sphere begins to subtly vibrate, a prelude to the impending collision. The moment of contact is captured in stunning detail, revealing the transfer of kinetic energy as the moving sphere’s momentum is transferred to the stationary one. The spheres, crafted from the same dense material, maintain their spherical shapes and masses, ensuring the conservation of momentum throughout the impact. The scene is illuminated by a single, soft light source, casting long shadows and emphasizing the physics of the collision. Fixed camera view, no camera movement."

### 20. 木球与铁立方的碰撞运动

- **具体描述**：木球与铁立方发生碰撞，碰撞过程遵循动量守恒定律，碰撞后二者沿各自轨迹运动
- **物理现象类型**：刚体碰撞运动
- **运动连续性**：非连续运动（碰撞为间断点）
- **物理参数**：木球与铁立方的质量、初始速度、动量守恒约束、恢复系数
- **完整prompt**：A wooden ball collides with an iron cube.

### 21. 苹果落地碰撞破碎现象

- **具体描述**：苹果从空中下落至坚硬地面，因碰撞发生破碎
- **物理现象类型**：重力下落-非弹性碰撞破碎运动
- **运动类型**：非连续运动（碰撞瞬间破碎）
- **物理参数**：苹果下落高度、地面硬度、苹果脆性系数、重力加速度$g$
- **完整prompt**："An apple falls on the hard ground"

### 22. 材料硬度现象（鸡蛋撞岩石破碎）

- **具体描述**：生鸡蛋以较大力度撞击岩石，鸡蛋因硬度远低于岩石而破碎，岩石保持完整
- **物理现象类型**：材料硬度主导的碰撞破坏
- **运动类型**：非连续运动（碰撞瞬间发生破坏）
- **物理参数**：鸡蛋与岩石的硬度值、撞击速度、重力加速度$g$
- **完整prompt**："a delicate, fragile egg is hurled with significant force towards a rugged, solid rock surface, where it collides upon impact"

### 23. 刚体拖动碰撞现象

- **具体描述**：刚体物体被拖动至立方体旁并发生碰撞，引发立方体位移
- **物理现象类型**：刚体拖动-碰撞运动
- **运动类型**：非连续运动（碰撞瞬间状态突变）
- **物理参数**：拖动速度、碰撞恢复系数、两物体质量、地面摩擦系数
- **物理参数**（无显式prompt，为实验场景描述）：物体初始间距、撞击角度

### 24. 多米诺骨牌受阻现象

- **具体描述**：多米诺骨牌链中间放置橡皮鸭，骨牌倾倒至橡皮鸭处时运动中断，仅单侧骨牌完成倾倒
- **物理现象类型**：刚体链传动-障碍中断运动
- **运动类型**：非连续运动（障碍处运动中断）
- **物理参数**：骨牌间距、初始倾倒速度、橡皮鸭尺寸与位置
- **完整prompt**（场景描述）："a chain of dominoes with a rubber duck in the middle interrupting the chain"

### 25. 透明玻璃杯的注水运动

- **具体描述**：清水被缓慢倒入透明玻璃杯中，水在杯中形成液面并伴随液面上升与波纹扩散
- **物理现象类型**：流体运动（液面变化）
- **运动连续性**：连续运动
- **物理参数**：注水速率、玻璃杯形状（圆柱形）、水的密度
- **完整prompt**：Clean water is poured into a transparent glass.

### 26. 威士忌杯的注酒运动

- **具体描述**：琥珀色威士忌从酒瓶倒入酒馆木质桌面的威士忌杯，液体在杯中形成液面并产生波纹
- **物理现象类型**：流体运动（液面填充）
- **运动连续性**：连续运动
- **物理参数**：注酒速率、杯子形状、液体密度与粘度
- **完整prompt**：A whiskey glass on a wooden table in tavern, and amber-colored whiskey is poured into it from a bottle.

### 27. 油与水的分层运动

- **具体描述**：透明玻璃杯中的油被缓慢倒入水杯，因密度差异出现油水分层现象
- **物理现象类型**：流体分层运动
- **运动连续性**：连续运动
- **物理参数**：油与水的密度、注入速率、杯子形状
- **完整prompt**：A clear glass of oil is gently poured into a glass of water.

### 28. 流体泼洒现象（红液体浇橡皮鸭）

- **具体描述**：红色液体倾倒在橡皮鸭表面，沿鸭身轮廓流动并产生溅射
- **物理现象类型**：流体附着与溅射运动
- **运动类型**：连续运动
- **物理参数**：液体流速、液体粘度、橡皮鸭表面粗糙度、重力加速度$g$
- **完整prompt**："Red liquid pouring on a rubber ducky"

### 29. 泥轮溅水坑现象

- **具体描述**：沾满泥浆的车轮驶过深水坑，引发泥水向四周飞溅
- **物理现象类型**：刚体运动-流体溅射复合现象
- **运动类型**：连续运动
- **物理参数**：车轮转速、水坑深度与粘度、泥浆附着系数、重力加速度$g$
- **完整prompt**："A muddy wheel splashes through a deep puddle"

### 30. 浮力现象（铁沉水）

- **具体描述**：铁块被轻放至水槽水面，因密度大于水而下沉
- **物理现象类型**：浮力作用下的下沉运动
- **运动类型**：连续运动
- **物理参数**：铁块密度、水的密度、重力加速度$g$
- **完整prompt**："A piece of iron is gently placed on the surface of the water in a tank filled with water"

### 31. 木块的水上漂浮运动

- **具体描述**：木块轻放至碗中水面，因浮力与重力平衡而保持漂浮
- **物理现象类型**：浮力平衡运动
- **运动连续性**：连续运动（静止为特殊连续状态）
- **物理参数**：木块质量与体积、水的密度、重力加速度$g$
- **完整prompt**：A piece of wood block is gently placed on the surface of a bowl filled with water.

### 32. 弹性材料外力形变现象

- **具体描述**：弹性物体（如弹性椅）在指定位置受外力拖动，发生可恢复性形变与位移
- **物理现象类型**：弹性形变与平动复合运动
- **运动类型**：连续运动
- **物理参数**：杨氏模量$E$、泊松比$\nu$、外力大小与方向、拖动点位置、地面高度$h$
- **完整prompt**："The chair was gently lifted upwards on the left seat back in a smooth, controlled motion, as if a gentle upwards force is dragging it on the left seat back. The background remains unchanged"

### 33. 形变现象

- **具体描述**：软面团/酸奶条被压平/铺展，形状随时间发生持续性变化
- **物理现象类型**：粘弹性形变运动
  - **运动类型**：连续运动

- **物理参数**：形变速率$\Delta l$、施加压力（隐含）、材料粘弹性系数（隐含）
- **完整prompt**："A piece of soft dough is evenly flattened on a workbench..."

### 34. 尺寸变化现象

- **具体描述**：气球在充气过程中直径随时间增大（增速渐缓）
- **物理现象类型**：体积膨胀运动
- **运动类型**：连续运动
- **物理参数**：膨胀速率$\Delta r$、初始体积、内部气压变化（隐含）
- **完整prompt**："A white balloon inflating in a cozy living room..."

### 35. 热学沸腾现象（水升温至100℃沸腾）

- **具体描述**：茶壶中的水温度快速升至100℃，发生液态到气态的相变并产生气泡
- **物理现象类型**：液体沸腾相变
- **运动类型**：连续运动（温度变化+气泡生成）
- **物理参数**：临界温度100℃、大气压强（标准大气压）、升温速率
- **完整prompt**："a timelapse capturing the transformation of water as the temperature rapidly rises above 100◦C"

### 36. 黄油的热熔化运动

- **具体描述**：黄油在温度升高时发生熔化，由固态变为半固态/液态并产生形态变化
- **物理现象类型**：热致相变运动
- **运动连续性**：连续运动
- **物理参数**：温度变化速率、黄油熔点、热传导系数
- **完整prompt**：A timelapse captures the gradual transformation of butter as the temperature rises significantly.

### 37. 浓硫酸与棉花的热化学作用

- **具体描述**：浓硫酸倾倒在棉花上，发生脱水与放热反应，棉花逐渐碳化
- **物理现象类型**：热化学运动（非纯物理，含化学变化伴随物理形变）
- **运动连续性**：连续运动（反应过程连续）
- **物理参数**：浓硫酸浓度、棉花质量、反应放热速率
- **完整prompt**：A timelapse captures the reaction as concentrated sulfuric acid is poured onto a cotton ball.

### 38. 光学反射现象（风筝水面倒影）

- **具体描述**：风筝在平静池塘上方飞行，水面呈现其清晰倒影
- **物理现象类型**：镜面反射现象
- **运动类型**：连续运动（风筝运动+反射成像同步变化）
- **物理参数**：水面平整度、光线入射角与反射角、风筝高度与姿态
- **完整prompt**："a kite soaring above a smooth and tranquil pond"

### 39. 白板笔的书写运动

- **具体描述**：蓝色马克笔在光滑白色白板表面进行书写，笔尖与板面接触并产生连续笔迹
- **物理现象类型**：刚体平面运动（笔尖轨迹运动）
- **运动连续性**：连续运动
- **物理参数**：笔尖运动速度、书写压力、白板与笔尖的摩擦系数
- **完整prompt**：A blue marker is used to write on the smooth, white surface of a whiteboard



## PhysCtrl - 力学现象

ObjaverseXL: 获取高质量3D物体

 MPM simulator: 对每个物体进⾏动画模拟

固定数量的模拟点 N = 2048（在⽹格⾯上均匀采样）和帧数 F = 24

数据增强环节：将物体绕$y$轴随机旋转，并向每个采样得到的初始点添加噪声$$\epsilon_p^{aug} \sim \mathcal{N}(0, 0.01^2)$$。

数据集包含550k个物体，其中包括150k个不同拖拽力方向的弹性物体，以及分别对应弹性、沙子、橡皮泥和刚性材料的100k个受重力作用的物体。

对于拖拽力可变的模拟动画，我们随机采样一个恒定力$$\mathbf{f}$$、一个属于初始点云$$\mathbf{P}_0$$的拖拽点$$\mathbf{D}$$，以及物理参数$$E \in [10^4, 10^7]$$、$$\nu \in [0.05, 0.45]$$。力$$\mathbf{f}$$的方向沿物体表面向外，其总幅值介于$$0.02G$$到$$0.3G$$之间（$$G$$为物体的总重力），且仅作用于拖拽点$$\mathbf{D}$$附近的点。

### 物理现象

1. **多材料的形变与运动**
   - 弹性材料（elastic）的弹性形变与恢复；
   - 塑性材料（plasticine）的塑性形变（不可恢复形变）；
   - 颗粒材料（sand）的颗粒流运动与堆积；
   - 刚性材料（rigid）的刚体平移与旋转。
2. **外力驱动的动力学响应**
   物体在指定外力作用下的位移、形变，以及运动轨迹的时间演化，包含单一点/区域的拖拽、重力作用等场景。
3. **边界约束交互**
   物体与地面的接触约束（防止穿透地面），以及初步探索的**多物体碰撞**（如物体向立方体移动并发生碰撞的场景）。
4. **连续介质力学相关现象**
   基于材料点法（MPM）的变形梯度演化、应力-应变关系等连续介质动力学行为。

**具体物理参数**

论文中实验所用的物理参数分为**核心控制参数**、**材料本构参数**、**仿真与模型参数**三类：

1. **核心控制参数**
   - **外力（f）**：作用于物体表面的恒定外力，方向为物体表面向外，大小范围为物体总重力（G）的0.02G~0.3G，仅施加在拖拽点（D）附近的点；
   - **拖拽点（D）**：属于初始点云$P_0$的三维坐标点，为外力作用的核心区域；
   - **地面高度（h）**：场景的边界约束参数，用于限制物体点云不穿透地面。
2. **材料本构参数**
   - **杨氏模量（E）**：针对弹性材料，取值范围为$[10^4, 10^7]$，可控制材料的刚度（如论文图1中展示了$E=10^4$和$E=10^5$的不同形变效果）；
   - **泊松比（ν）**：取值范围为$[0.05, 0.45]$，论文验证其对生成轨迹影响可忽略（与PhysDreamer结论一致）；
   - **材料类型（[mat]）**：离散型参数，包含elastic、sand、plasticine、rigid四类，作为模型的条件输入。
3. **仿真与模型参数**
   - **点云数量（N）**：每个物体固定为2048个点，用于表征物体几何与动力学；
   - **时间步与帧数**：仿真帧数$F=24$；MPM仿真子步$\Delta t$（远小于帧间隔$\Delta T$）；
   - **密度（ρ）**：连续介质力学中的基础参数，参与动量守恒方程计算；
   - **变形梯度（F）**：表征材料局部的旋转与拉伸，通过MPM方程约束其更新（公式3、公式8）。

此外，在物理参数估计实验中，还针对**杨氏模量（E）**的对数形式$log_{10}(E)$​进行误差评估，其平均绝对误差（MAE）为0.506（相较于可微分MPM的0.394~0.439，效率提升显著）。



### Prompt

#### GPT-4o评估专用Prompt

You are tasked with evaluating the quality of image-to-video generation produced by a model.
For each test case, you will be given: 1. A text prompt describing a single object and a force applied to it. The force’s position and direction are visualized as a red arrow in the input image. 2. An input image of the object. 3. Five sets of 10 evenly spaced frames-each set corresponds to a video generated by a different model from the same input.
Please evaluate this video based on the following three criteria using a 5-point Likert scale (1 = poor, 5 = excellent):

- Semantic Adherence: How well the content and motion in the video match the description in the text prompt, especially the alignment with the force direction and position. Note that the video should starts with the input image.
- Physical Commonsense: Whether the object’s motion follows intuitive, physically plausible dynamics given the applied force direction and position.
- Video Quality: The overall visual and temporal quality of the video (note that static or nearly-static sequences are less preferred).
  Provide your evaluation for each video strictly in the following one-line format:
  Video i, Semantic Adherence score, Physical Commonsense score, Video Quality score

#### 视频生成任务文本Prompt

1. **刚性/弹性材料局部受力位移**

- The chair was gently lifted upwards on the left seat back in a smooth, controlled motion, as if a gentle upwards force is dragging it on the left seat back. The background remains unchanged

2. **刚性材料刚体复合运动**

- A futuristic spiked UFO hovers above glowing clouds at sunset. It rotates counter clockwise and moves faraway with a steady motion.

3. **刚性/柔性材料刚体旋转运动**

- An orange starfish rotating clockwise towards the right, creating a smooth and natural motion

4. **弹性/塑性材料中心受力形变与位移**

- A soft, striped blanket lies flat on the ground, then slowly lifts upwards as if an upward force is dragging it in the middle

5. **刚性材料刚体姿态调整与平动**

- A fighter jet flies at high speed in the sky and its nose tilts upward, lifting the entire aircraft

6. **刚性材料局部受力整体位移**

- A pair of wireless headphones rests on a white table before lifting into the air, as if there is an invisible force applied to its handle

7. **刚性材料非对称外力驱动整体位移**

- the penguin is fully lifted upwards and float into the air with a natural motion, as if there is a force applied onto its left wing

8. **刚性材料斜向外力驱动复合位移**

- the giraffe is dragged upwards toward the left and floating into the air with a natural motion, as if there is an upper left force.

此外，论文还提及了多物体碰撞的初步实验，即物体被拖拽撞击立方体的场景，其对应的物理现象为多刚体接触碰撞动力学



## NEWTONGEN - 运动/形变



### 物理现象

本文实验针对**12类牛顿物理运动/形变现象**展开，统一采用9维潜物理状态$Z=[x,y,v_x,v_y,\theta,\omega,s,l,a]$表征（$x/y$为质心位置、$v_x/v_y$为质心速度、$\theta$为旋转角度、$\omega$为角速度、$s/l$为最短/最长维度、$a$为投影面积），通用参数范围为**速度0–15 m/s**、**运动时长1–2秒**，以下为各类现象专属参数：

| 物理现象         | 核心评估物理量（PIS指标）                   | 初始/控制参数                                                | 潜物理状态约束                                               |
| ---------------- | ------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 匀速运动         | $v_x$（水平速度）                           | 物体沿光滑表面水平匀速移动，无外力干扰                       | $v_x$恒定、$v_y≈0$、$\omega=0$、$s/l/a$无变化                |
| 匀加速运动       | $a_x$（水平加速度）                         | 物体沿平直路面从低速/静止开始水平匀加速                      | $a_x$为固定正值、$v_x$线性增长、$\omega=0$、$s/l/a$无变化    |
| 匀减速运动       | $-a_x$（水平减速加速度）                    | 物体沿道路从高速开始水平匀减速                               | $a_x$为固定负值、$v_x$线性降低、$\omega=0$、$s/l/a$无变化    |
| 抛物运动         | $v_x$（水平速度）、$a_y$（竖直加速度）      | 物体以固定角度斜抛，如初始位置$[x=2.0,y=10.0]$、初始速度$[v_x=5.0m/s,v_y=-0.8m/s]$ | $v_x$恒定、$a_y$近似重力加速度、$\omega=0$、$s/l/a$无变化    |
| 3D运动           | $v_y$（竖直速度）、$\Delta l$（长轴增量率） | 物体从远处向镜头移动，模拟近大远小                           | $v_y$恒定、$\Delta l$均匀增大、$l/s$比例不变、$\omega=0$     |
| 斜面滑动         | $a_x$（水平加速度）、$a_y$（竖直加速度）    | 物体沿光滑斜面由静止下滑                                     | $a_x/a_y$为固定分量、$\omega=0$、$s/l/a$无变化               |
| 圆周运动         | $\omega$（轨道角速度）                      | 天体绕中心公转，如初始位置$[x=12,y=4]$、初始角速度$\omega=1.0rad/s$、世界尺寸$18×12$ | $\omega$恒定、$x/y$呈圆周轨迹、$s/l/a$无变化                 |
| 定轴转动         | $\omega$（自转角速度）                      | 物体绕自身轴线转动，无水平位移                               | $\omega$恒定、$\theta$线性增加、$v_x=v_y=0$、$s/l/a$无变化   |
| 带自转的抛物运动 | $v_x$、$a_y$、$\omega$（自转角速度）        | 物体斜抛且伴随自转，如画笔/钢笔抛射                          | 同时满足抛物轨迹（$v_x/a_y$恒定）和匀速自转（$\omega$恒定）  |
| 阻尼振动         | $a_y$（竖直加速度）                         | 悬挂铃铛/单摆小幅摆动，悬挂点固定                            | $a_y$近似恒定、$y$位置周期性衰减、$\omega$随摆角周期变化、$x$固定 |
| 尺寸变化         | $\Delta r$（半径增量率）                    | 气球均匀充气，初始尺寸$s=0.3/0.6$                            | $\Delta r$恒定、$s/l/a$均匀增大、$l/s$比例不变、$v_x=v_y=\omega=0$ |
| 形变             | $\Delta l$（长轴增量率）                    | 面团/酸奶均匀摊平，初始为长条状                              | $\Delta l$恒定、$l$增大且$s$可减小、$a$随面积变化、$v_x=v_y=\omega=0$ |

注：所有现象均采用**5帧移动平均滤波**预处理视频，以$0.00625米/像素$完成像素-物理单位映射，PIS值越接近1表示物理一致性越强。

### Prompt


1. Uniform Motion（匀速运动）
- Prompt 1：A small metal cube sliding steadily along a smooth laboratory bench, reflections visible on the surface, scattered tools in the background, captured from a fixed side camera.  
- Prompt 2：A red rubber ball rolling at constant speed on a polished wooden floor, pulled by a thin string, with scattered papers and books in the background, observed from a fixed side camera.  


2. Acceleration（匀加速运动）
- Prompt 1：A red sedan accelerating in a straight line on a clean highway, the road flat and clear, with only a pale sky and distant horizon in the background, captured from a fixed roadside camera.  
- Prompt 2：A black off-road SUV accelerating in a straight line on sandy terrain, with continuous sand dunes in the background, a few white clouds in the sky, sunlight slanting, kicking up fine sand particles, viewed from a stationary side-angle camera.  


3. Deceleration（匀减速运动）
- Prompt 1：A yellow bus decelerates in a straight line in front of a traffic light on a city street, with pedestrians crossing nearby, and the wet road reflecting the sky, captured by a fixed side-view camera.  
- Prompt 2：A red coach brakes and decelerates in a straight line on a highway, with road signs and streetlights nearby and the city skyline visible in the distance, captured by a fixed side-view camera.  


4. Parabolic Motion（抛物运动）
- Prompt 1：A golf ball is hit at an angle with an initial speed. The camera captures its parabolic trajectory from the side. The scene takes place on a sunny golf course with manicured fairways, sand bunkers, and distant trees, adding depth and realism.  
- Prompt 2：A volleyball is served at an angle, captured from the side by a stationary camera. The scene is set on an outdoor beach volleyball court, with sand texture, net, and distant palm trees in view.  


5. 3D Motion（3D运动）
- Prompt 1：A fighter jet accelerates slowly from the distance along the runway towards the camera, hangars and runway lights visible in the background, captured from a fixed oblique side camera.  
- Prompt 2：A cardboard box slides from the distance along a warehouse floor towards the camera, shelves and crates visible in the background, captured from a fixed oblique side camera.  


6. Slope Sliding（斜面滑动）
- Prompt 1：A hardcover book accelerating down a carpeted inclined board in a classroom, chalkboard and desks in the background, captured from a fixed side camera parallel to the ramp.  
- Prompt 2：A small metal cube sliding down a laboratory ramp, shiny reflections on its surface, scattered tools and wires in the background, captured from a fixed side camera parallel to the ramp.  


7. Circular Motion（圆周运动）
- Prompt 1：A tiny moonlet orbits a gas giant along a smooth, circular path. The top-down view shows the consistent motion without motion trails.  
- Prompt 2：A comet with a glowing tail orbits a distant star along a stable circular path. A top-down perspective emphasizes the symmetrical orbit and the stationary central star.  


8. Rotation（定轴转动）
- Prompt 1：A metal rod spinning on a concrete floor, faint scratches and dust visible, captured from a fixed top-down camera.  
- Prompt 2：A wooden dowel rotating gently on a tiled kitchen floor, soft shadows from ceiling lights, viewed from a stationary overhead camera.  


9. Parabolic Motion with Rotation（带自转的抛物运动）
- Prompt 1：A pen is thrown at an angle, rotating as it falls. Captured from a side camera, the notebook and desk provide background details and depth.  
- Prompt 2：A thin cylindrical rod gently tossed, rotating along its long axis, fixed side camera, realistic reflections, ground shadows visible, subtle motion blur.  


10. Damped Oscillation（阻尼振动）
- Prompt 1：A small decorative bell hanging from a fine chain. The fixed camera captures realistic material and shadows.  
- Prompt 2：A realistic pendulum with a spherical bob swinging from a fixed pivot. The fixed camera captures the entire motion.  


11. Size Changing（尺寸变化）
- Prompt 1：A red helium balloon gradually inflating in a sunny park, children playing in the background, trees casting soft shadows, captured from a stationary side camera.  
- Prompt 2：A transparent water balloon expanding in a laboratory, scientific instruments and glassware around, bright fluorescent lights overhead, captured from a fixed top-down camera.  


12. Deformation（形变）
- Prompt 1：A long strip of yogurt slowly spreads into a smooth layer, captured by a fixed overhead camera.  
- Prompt 2：A long strip of jelly gradually deforms and flattens on a plate, captured by a fixed overhead camera.