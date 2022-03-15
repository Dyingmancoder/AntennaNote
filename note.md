# 第一章 天线基础知识 ##
目录
- [第一章 天线基础知识](#第一章-天线基础知识)
  - [1.1 基本振子的辐射](#11-基本振子的辐射)
    - [1.1.1 电基本振子的辐射](#111-电基本振子的辐射)
## 1.1 基本振子的辐射 ##
### 1.1.1 电基本振子的辐射 ###
1. **电基本振子**是一段有高频电流，且带有等值异号电荷的短导线，其直径`d << l`，`（长度）l << λ（波长）`。
2. 电基本振子在空间所产生的的电磁场可通过**矢量磁位A**求得，矢量磁位A的计算公式为
   $$\vec{{A}}=\iiint\mu\vec{J}\frac{e^{-jkR}}{4\pi R}dv'$$
   式中，$R=\sqrt{(x-x')^2+(y-y')^2+(z-z')^2}$为源点到场点的距离，$(x',y',z')$为源点的坐标，$(x,y,z)$为场点的坐标。
3. 由电流所产生的的矢量磁位，再通过$\vec{B}=\nabla\times\vec{A}$得
   $$\vec{H}=\frac{1}{\mu}\nabla\times\vec{A}$$
4. 由麦克斯韦第一方程$\nabla\times\vec{H} = j\omega E$得
   $$\vec{E}=\frac{1}{j\omega\epsilon}\nabla\times\vec{H}$$
   就可以计算由电基本振子在空间所产生的电磁场。
5. 设电基本振子位千坐标原点，轴线沿z轴，点基本振子为线元，则矢量磁位的积分中$\vec{J}dV'$可用$\vec{I(z)=Idz\vec{e_x}}$代替，带入之前的式子中可得其在空间所产生的矢量磁位为
   $$\vec{A}=\vec{e_x}\frac{\mu\vec{I}}{4\pi}\int_{-\frac{l}{2}}^{\frac{l}{2}}\frac{e^{-jkR}}{R}dz'$$
   采用近似有
   $$\vec{A_x}=\frac{\mu Il}{4\pi r}e^{-jkr}$$
   将$\vec{e_x}=\vec{e_r}\cos\theta-\vec{e_\theta}\sin\theta$带入有
   $$\left\{
       \begin{aligned}
           A_r=A_z\cos\theta=\frac{\mu Il}{4\pi r}e^{-jkr}\cos\theta\\
            A_\theta=-A_z\sin\theta=-\frac{\mu Il}{4\pi r}e^{-jkr}\sin\theta\\
            A_\varphi = 0
       \end{aligned}
       \right.$$
    将上式带入之前的矢量磁位以及麦克斯韦第一方程，得电基本振子的电磁场为
    $$\left\{
        \begin{aligned}
            E_r=\frac{Il}{4\pi}\frac{2}{\omega\epsilon}\cos\theta[\frac{k}{r^2}-\frac{j}{r^3}]e^{-jkr}\\
            E_r=\frac{Il}{4\pi}\frac{1}{\omega\epsilon}\sin\theta[j\frac{k^2}{r}+\frac{k}{r^2}-\frac{j}{r^3}]e^{-jkr}\\
            E_\varphi = 0\\
            H_r=H_\theta=0\\
            H_\varphi=\frac{Il}{4\pi}\sin\theta[\frac{jk}{r}+\frac{1}{r^2}]e^{-jkr}
        \end{aligned}
        \right.$$
    式中，$k=\frac{2\pi}{\lambda}=\omega\sqrt{\mu\epsilon}$为相移常数(波数)，$\epsilon$为介电常数，$\mu$为磁导率。在自由空间中，$\epsilon=\epsilon_0=\frac{1}{36\pi}\times 10^{-9}F/m,\mu=\mu_0=4\pi\times 10^{-7}H/m$。
6. 电基本振子所产生的的电磁场有以下特点：
   - 电场仅有$E_r$和$E_\theta$两个分量，磁场仅有$H_\varphi$分量，三个场分量相互垂直；
   - 电力线在子午面内(含z轴的平面)，磁力线在赤道面内(垂直于z轴平面)；
   - 电磁场的各分量均随r的增大而减小，每个分量的表达式中的不同项随r的增大而减小的速度不同。当$kr$很小时，$\frac{1}{kr}$最小，$\frac{1}{(kr)^3}$最大。但$\frac{1}{kr}$随着$kr$的增大衰减速度最慢，所以当$kr$较大时，$\frac{1}{kr}$变为最大。
7. 近区
   - 近区场电磁场的简化表示式：
    $$\left\{
        \begin{aligned}
            E_r=-j\frac{Il}{4\pi r^3}\frac{2}{\omega\epsilon}\cos\theta\\
            E_\theta=-j\frac{Il}{4\pi r^3}\frac{1}{\omega\epsilon}\cos\theta\\
            E_\varphi=0\\
            H_r=H_\theta=0\\
            H_\varphi=\frac{Il}{4\pi r^2}\sin\theta
        \end{aligned}
        \right.$$
    - 电基本振子的近区场有如下特点：
      - $E_r$和$E_\theta$与静电场问题中点偶极子的电场相似，而$H_\varphi$和恒定电流元的磁场相似。因此，近区又称为似稳区，近区场又称为似稳场。
      - 近区场随距离r的增大迅速减小，因此在离开天线较远的地方，近区场变得很小。
      - 电场相位滞后于磁场相位90°，因而玻印亭矢量是纯虚数，近场区每周期平均辐射的功率为0.
8. 远区
   - 远区场电磁场的简化表达式：
    $$\left\{
        \begin{aligned}
            E_\theta=j\frac{Il}{4\pi r}\omega\mu\sin\theta e^{-jkr}=j\frac{Il}{4xr}\eta\sin\theta e^{-jkr}\\
            H_\varphi=j\frac{Il\omega\sqrt{\mu\epsilon}}{4\pi r}\sin\theta e^{-jkr}=j\frac{Il}{2\lambda r}\sin\theta e^{-jkr}\\
            E_r\approx0\\
            H_r=H_\theta=E_\varphi=0
        \end{aligned}
        \right.$$
    - 远区场的特点如下：
      - 远区场仅有$E_\theta$和$H_\varphi$两个分量，两者在时间上同相，在空间上互相垂直，并与矢径r方向垂直。玻印亭矢量$\vec{S}=\frac{1}{2}\vec{E}\times\vec{H^*}$是纯虚数，方向为矢径r的方向。**可见，电基本振子在远区的场是一沿着径向向外传播的恒电磁波。电磁能量离开长远向空间辐射，不再返回，这种场成为辐射场。**
      - $E_\theta$和$H_\varphi$两个分量均与$\frac{1}{r}$成正比，是由扩散引起的。当距离增加时，场强相对于近场区减少得比较缓慢，因而可以传播到离发射天线很远的地方。
      - 电基本振子的辐射场与$\sin\theta$成正比，即在不同$\theta$方向上，它的辐射强度是不同的，在$\theta$等于0°和180°方向上，即振子轴线的方向上辐射为零，而在同过振子中心并垂直于振子轴线的方向上，即$\theta=90°$方向，辐射最强。因此辐射场是有**方向性的**，其辐射方向图如下图所示
      - $E_\theta$和$H_\varphi$的比值为$\frac{E_\theta}{H_\varphi}=\sqrt{\frac{\mu}{\epsilon}}=\eta(\Omega)$，是一个实数，成为波阻抗。**在自由空间中$\eta=\eta_0=120\pi(\Omega)$。** 将此公式带入可得自由空间中电流元辐射场的实用表达式：
    $$\left\{
            \begin{aligned}
                \vec{E}=E_\theta e_\theta=j\eta_0\sin\theta e^{-jkr}=j\frac{60\pi Il}{\lambda r}\sin\theta e^{-jkr}\vec{e_\theta}\\
                \vec{H}=H_\varphi e_\varphi=j\frac{Il}{2\lambda r}\sin\theta e^{-jkr}\vec{e_\varphi}
            \end{aligned}
    \right.$$
        