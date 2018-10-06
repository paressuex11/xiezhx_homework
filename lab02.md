# 用Construct 2制作 personal Ghost Shooter

## 一些前话
Construct 2 采用面向对象编程范式，把相关功能都封装在对象里，使用者仅需理解对象间的行为即可。

Ghost Shooter是一款作为official Beginner's Guide的简单游戏，本文希望通过制作它的'Personal Edition'来加深对construct 2引擎的理解。

### Ghost Shooter游戏逻辑

人类射击怪兽，打死怪兽能计分，分数累计到一定量，则人类胜利，人类与怪兽接触会令人类死亡。

所需对象：人类(player), 怪兽(monster), 子弹(bullet), UHD, Background,system,mouse,keyboard,explode

实现效果大致如下：

![](/images/giff.gif)

###图层(layers)

construct 2里把游戏结构划分成很多层(layers)，设计者可以在这些图层中放置对象，层与层之间难以互相干扰，利用这个特性，我们很容易想到

