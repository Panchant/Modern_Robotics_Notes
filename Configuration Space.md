---
tags:
  - Robotics
---
---

*Definition:* The **configuration** of a robot is a complete specification of the position of every point of the robot. The minimum number n of real-valued coordinates needed to represent the configuration is the number of **degrees of** **freedom (dof)** of the robot. The n-dimensional space containing all possible configurations of the robot is called the **configuration space (C-space)**. The configuration of a robot is represented by a point in its C-space.

# 1. Degrees of Freedom of a Rigid Body

1.1 Degrees of freedom = (sum of freedoms of the points) − (number of independent constraints).

1.2 Degrees of freedom = (number of variables) − (number of independent equations).

We have just established that a rigid body moving in three-dimensional space, which we call a **spatial rigid body**, has six degrees of freedom. Similarly, a rigid body moving in a two-dimensional plane, which we henceforth call a **planar rigid body**, has three degrees of freedom.

1.3 Equation (1.1) can be expressed as follows: Degrees of freedom = (sum of freedoms of the bodies) − (number of independent constraints).

---
# 2. Degrees of Freedom of a Robot

## 2.1 Robot Joints

The **revolute joint (R)**, also called a hinge joint, allows rotational motion about the joint axis. The **prismatic joint (P)**, also called a sliding or linear joint, allows translational (or rectilinear) motion along the direction of the joint axis. The **helical joint (H)**, also called a screw joint, allows simultaneous rotation and translation about a screw axis. Revolute, prismatic, and helical joints all have one degree of freedom.

![捕获.PNG](https://img.picui.cn/free/2025/05/26/683486b0a6d4d.png)

The **cylindrical joint (C)** has two degrees of freedom and allows independent translations and rotations about a single fixed joint axis. The **universal joint (U)** is another two-degree of-freedom joint that consists of a pair of revolute joints arranged so that their joint axes are orthogonal. The **spherical joint (S)**, also called a ball-and-socket joint, has three degrees of freedom and functions much like our shoulder joint

![捕获.PNG](https://img.picui.cn/free/2025/05/26/6834875c1b992.png)

A joint can be viewed as providing freedoms to allow one rigid body to move relative to another. It can also be viewed as providing constraints on the possible motions of the two rigid bodies it connects.

![微信图片_20250526232953.png](https://img.picui.cn/free/2025/05/26/683488f559506.png)

- **Revolute (R) - 转动副:**
    
    - **dof f=1:** 只允许一个相对转动自由度。
    - **Planar c=2:** 在平面内，转动副约束了两个平移自由度。 (3−1=2)
    - **Spatial c=5:** 在空间中，转动副约束了三个平移自由度和两个转动自由度。 (6−1=5)
- **Prismatic (P) - 移动副:**
    
    - **dof f=1:** 只允许一个相对移动（滑动）自由度。
    - **Planar c=2:** 在平面内，移动副约束了一个平移自由度和一个转动自由度。 (3−1=2)
    - **Spatial c=5:** 在空间中，移动副约束了两个平移自由度和三个转动自由度。 (6−1=5)
- **Helical (H) - 螺旋副:**
    
    - **dof f=1:** 允许一个与转动成比例的移动自由度（类似于螺丝）。
    - **Planar c=N/A:** 螺旋运动通常在空间中定义，在纯粹的平面情况下没有直接对应的概念。
    - **Spatial c=5:** 在空间中，螺旋副约束了两个平移自由度和三个转动自由度，但保留了一个耦合的转动和平移自由度。 (6−1=5)
- **Cylindrical (C) - 圆柱副:**
    
    - **dof f=2:** 允许一个轴向移动自由度和一个绕该轴的转动自由度。
    - **Planar c=N/A:** 圆柱运动是空间概念。
    - **Spatial c=4:** 在空间中，圆柱副约束了两个平移自由度和两个转动自由度。 (6−2=4)
- **Universal (U) - 万向节 (虎克铰):**
    
    - **dof f=2:** 允许绕两个相互垂直的轴转动。
    - **Planar c=N/A:** 万向节是空间概念。
    - **Spatial c=4:** 在空间中，万向节约束了三个平移自由度和一个转动自由度。 (6−2=4)
- **Spherical (S) - 球副:**
    
    - **dof f=3:** 允许绕三个相互垂直的轴转动（类似于球窝接头）。
    - **Planar c=N/A:** 球运动是空间概念。
    - **Spatial c=3:** 在空间中，球副约束了三个平移自由度。 (6−3=3)