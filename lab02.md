# 用Construct 2制作 personal Ghost Shooter

## 一些前话
Construct 2 采用面向对象编程范式，把相关功能都封装在对象里，使用者仅需理解对象间的行为即可。

Ghost Shooter是一款作为official Beginner's Guide的简单游戏，本文希望通过制作它的'Personal Edition'来加深对construct 2引擎的理解。

## Ghost Shooter游戏逻辑

人类射击怪兽，打死怪兽能计分，分数累计到一定量，则人类胜利，人类与怪兽接触会令人类死亡。

所需对象：人类(player), 怪兽(monster), 子弹(bullet), UHD, Background,system,mouse,keyboard,explode

实现效果大致如下：

![](/images/giff.gif)

![](/images/7.png)

## 图层(layers)

construct 2里把游戏结构划分成很多层(layers)，设计者可以在这些图层中放置对象，层与层之间难以互相干扰，利用这个特性，我们很容易想到把互不干扰的对象放在不同的层。例如：背景对象不会干扰其他对象，UHD对象同理，于是我们把这两个对象分别放在不同layers。

![](/images/1.png)

我们将游戏的主要部分放在 **main** 层里，其他层方便起见先暂时lock。

### sprite(精灵)

*construct 2* 把那些参与游戏的自建对象叫做sprite，我们主要将player,monster,bullet,explode对象放在 **main** 这一层里。这里也是最富有个性化的版块了，操作者可以用任意他们喜欢的图片来作为游戏对象(前提是合法)。

![插入Player对象](/images/2.png)

#### player

笔者这里采用的是时下较为热门的元气骑士形象。

![](/images/Knight.png)

player的主要行为是能向四面八方行走，视线总是跟着鼠标，发射子弹，这里有些行为不能仅通过behavior来解决，但我们最直观的的设计逻辑就是如此。

四面八方行走可以通过behavior来实现

![](/images/3.png)

实现效果如下：

![](/images/gifff.gif)

但与其他对象的互动就需要通过 **event** 来操作了。

#### monster

monster对象的行为主要是朝着player行走，这里同样涉及对象间的互动需要通过 **event** 系统来解决。但我们可以退而求其次，先设定一个直线行走。

![](/images/4.png)

#### bullet

bullet对象仅需要一往无前，但默认速度可能并不足以让Knight打败小怪兽，所以给Bullet加上一罐满满的燃料，
并且bullet消失后应被删除，减少内存负担

![](/images/giffff.gif)

同时我们需要削弱怪兽的速度，以防英雄一出现就挂了。

#### explode

explode的存在意义仿佛就是消失。在Bullet与monster碰撞后生成的explode，在0.5秒后消失。

要是想去掉explode背景的黑色还需调整如下：

![](/images/5.png)

## event

**event** 系统，遵循condition-action操作，达成condition就会触发action。

例如：让player总是看着鼠标

![](/images/6.png)

这种涉及多对象的操作便可以通过 **event** 系统来达成。

还有像在 **bullet碰撞monster时生成explode** *点击鼠标左键在player上生成bullet* ，乃至还可以为monster和player加上属性(attributes)，比如健康值，让游戏更加丰富多彩