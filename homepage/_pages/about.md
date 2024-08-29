---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

大家好！我是 **Long Yujie**，目前是本科三年级，就读于[武汉大学国家网络安全学院](https://cse.whu.edu.cn/)信息安全专业。

我对网络安全和人工智能充满热情，自入学以来，积极参与各类科研项目和学术竞赛，曾获得多项校内外奖项。在科研方面，我参与并主导了多个项目，包括但不限于**推荐系统**、**多模态**、**Geo AI**、**人工智能安全**、**多媒体信息内容安全**等领域。

# 🎓 Education Background

- **排名：平均学分绩点排名： 4/147 (2%)
- **成绩均分：**GPA：3.95/4.0、加权平均分：92.88/100
- **语言能力：**以良好成绩通过 CET4(596)、CET6(553)；具备良好的英语文献阅读和写作能力
- **核心课程：**高等数学 (95,96)、线性代数 (95)、概率论与数理统计 (97)、数据结构 (96,96)、离散数学 (94)、信息安全数学基础 (95)、编译原理 (97)、计算机网络 (93)、密码学 (97,93)、安全创客实践 (98)
- **编程能力：**熟练掌握 C++ 和 Python、熟悉算法与数据结构，抽象能力强，代码风格良好；熟练掌握 PyTorch、Numpy、Pandas
- **开发工具：**VS Code, PyCharm, Jupyter Notebook, LaTeX (Overleaf), Git
- **在校荣誉：**曾获武汉大学阮立平奖学金 (￥6000，全院共 2 人)、武汉大学三好学生 (10%)、武汉大学社会活动积极分子及多项竞赛奖金

# 🔥 News

- *2024.05*：  🎉🎉 我们的作品**HaMonitorSentry**在2024年第17届中国大学生计算机设计大赛(中南地区赛)中以**人工智能应用组一等奖**兼**第一名**的成绩**晋级国赛**！
- *2024.05*：  🎉🎉 我们的作品**FuzzLLM**在2024年第17届中国大学生计算机设计大赛(中南地区赛)获得**一等奖**！

# 🧪 Research Experience

## **💡💡💡CLIP4Rec - 基于 CLIP 的通用推荐框架研究**

- **时间：** 2023.9 - 2024.7
- **领域：** **点过程**，**最优传输**
- **角色：** 第三作者
- **针对痛点**：
  1. 时序点过程 (TPPs) 是对连续时间域上离散事件点进行建模的强大工具，已被广泛用于地震预测、金融分析、推荐系统等多个领域;
  2. 对于事件序列，通常存在一个分支过程来捕获隐藏在序列中的事件级触发模式，这个分支过程提供了对事件之间因果关系的洞察，帮助我们识别触发后续事件级联的关键事件，这对于揭示事件产生和信息扩散的潜在机制至关重要，如: 识别信息扩散网络中的信息来源或操纵关键节点以减轻特定信息的扩散;
  3. 推断事件分支有着重要意义，但其同样十分具有挑战性，因为事件分支是在实践中无法观察到的潜在变量：对于一些传统 TPP 如 Hawkes Process，我们可以在 EM 框架中根据观察到的事件序列来学习 TPP，其中事件分支通常被推断为事件的 responsibilities；对于 Transformer Hawkes Process 和 Self- attention Hawkes Process 等神经 TPP，模型内的 Attention Map 则可以作为事件分支的证据;
  4. 然而这两种方法都存在过平滑的问题，往往会推断出非结构化的事件分支；
  5. 目前亟需一种简单但有效的解决方案来准确推断各种 TPP 模型的结构增强事件分支。

* **我们的方法**：
  1. 引入了一种新的即插即用模块，该模块基于 Bregman Alternating Direction Method ofMultipliers 算法，在时间点过程 (TPPs) 的 MLE 框架中推断与事件序列相关的事件分支;
  2. 具体来说，我们的 BADMM 模块可以在行归一化的下三角矩阵上施加低秩和稀疏结构，当通过 EM 算法学习经典TPP(例如 Hawkes Process) 时，我们可以利用 BADMM 模块在 E 步中导出结构化 responsibilities 矩阵;
  3. 类似地，我们的 BADMM 模块也有助于为具有自注意层的神经 TPP 导出低秩和稀疏的 attention maps;
  4. 上述的结构化 responsibilities 矩阵和 attention maps 则都可以有效表征事件分支；在合成数据和现实数据上的实验均表明：将我们的 BADMM 模块插入到现有的 TPP 模型和学习范式中可以稳定提高模型的性能，并产出可解释的事件分支，对揭示事件产生和信息扩散的潜在机制提供了有价值的见解。
* **项目成果**：
  * 论文已投稿于**AAAI 2025**（第三作者，第一本科生作者）

## **💡💡HaMonitorSentry - 高层建筑智能监测系统** <sub> &nbsp;&nbsp;[[项目主页]](https://mumuyeye.github.io/HaMonitorSentry/README.html) | [[项目代码]](https://github.com/mumuyeye/HaMonitorSentry) </sub>

- **时间：** 2023.1 - 2024.5
- **领域：** **计算机视觉**，**Geo AI**
- **角色：** 主力队员
- **针对痛点**：
  1. **高层建筑监测局限性**：当前的监测系统主要聚焦于高空抛物，应用范围有限且性能不理想。常见问题包括实时性不足以及较高的漏检和错检率。
  2. **复杂场景下的挑战**：现有的运动目标检测与跟踪技术在复杂场景下尚未成熟，小目标快速检测尤其困难。
  3. **天气因素的影响**：监测效果受天气因素影响较大，这增加了对算法进行进一步优化的迫切需求。
- **我们的方法**：
  1. **引入轻量化的语义分割网络和知识蒸馏技术**：使用这些技术精确识别视频中的建筑物区域，定位可能的抛物区域，有效减少环境干扰。
  2. **采用背景差分法和帧差法**：根据环境变化和亮度条件的不同，这些方法提高了目标检测的速度和准确度。
  3. **结合2D和3D网络，利用自注意力机制**：这种结合方式融合时空信息，显著提高高层动作识别的精度。
  4. **构建专门的高层场景危险动作识别数据集并进行网络微调**：通过这种方法，能够更精确地识别和响应高层建筑中的潜在危险动作。

* **项目成果**：
  * 该项目成功申请为省级大学生创新创业项目，并在期限内以优秀的成绩结项。
  * 基于此项目成功申请了1项国家发明专利（第一作者）和2项软件著作权。&nbsp;<span style="font-size: 16px;">
    <a href="..\docs\sentryzhuanli.png">[专利]</a> &nbsp;|&nbsp;
    <a href="..\docs\sentryruanzhu1.png">[软著1]</a> &nbsp;|&nbsp;
    <a href="..\docs\sentryruanzhu2.png">[软著2]</a>
  * 参加第17届中国大学生计算机设计大赛，并**以中南地区赛人工智能应用组第一名（1/314）的成绩进入全国总决赛**。

## **💡从“堆盒子”到动态规划** <sub> &nbsp;&nbsp;[[项目代码]](https://github.com/mumuyeye/From-Stacking-Boxes-to-Dynamic-Programming) | [[互动视频]](https://www.bilibili.com/video/BV1ojKvehEuq)</sub>

- **时间：** 2022.1 - 2022.05
- **领域：** **算法教学**，**算法可视化**
- **角色：** 团队(负责人)
- **针对痛点**：算法自身的抽象性往往是同学们算法学习的最大阻碍，而“化抽象为具象”的最佳方法便是对算法进行“可视化”。

* **我们的作品**：采用了与著名博主3Blue1Brown所同源的基于Python的数学动画制作引擎Manim来制作，自主编写3000余行代码，配合后期大量的代码微调、剪辑、AI处理搭配工作，最终得以完成本次作品。
* **项目成果**：
  * 我们将视频发布到了Manim爱好者的交流社群中，在本院同学之间进行测试反馈和迭代，再到各高中乃至高校进行应用推广，均收到了良好反馈。

# 🏆 Competition Awards

- **中国大学生计算机设计大赛：晋级国赛** *国家级* 2024 &nbsp;&nbsp;[[证明]](..\docs\2024jishe.pdf)
- **全国大学生数学竞赛：一等奖** *国家级* 2023 &nbsp;&nbsp;[[证明]](..\docs\shujingguoer.png)
- **“华中杯”大学生数学建模挑战赛：二等奖 (2 out of 2030 teams)** *国家级* 2023 &nbsp;&nbsp;[[证明]](http://www.hzbmmc.com/views/award/award-item.html?id=1663113745191030785&navigate=inform)
- **中国大学生计算机设计大赛 (中南地区赛)：一等奖 (第一名)** *省部级* 2024 &nbsp;&nbsp;[[证明]](..\docs\2024jishe.pdf)
- **中国大学生计算机设计大赛 (中南地区赛)：一等奖** *省部级* 2024 &nbsp;&nbsp;[[证明]](..\docs\2024jishe.pdf)
- **中国大学生计算机设计大赛 (中南地区赛)：二等奖** *省部级* 2024 &nbsp;&nbsp;[[证明]](..\docs\2024jishe.pdf)
- **中国高校计算机大赛-网络技术挑战赛 (全国选拔赛)：二等奖** *省部级* 2024 &nbsp;&nbsp;[[证明]](..\docs\2024CCCCASTxuanbasai.pdf)
- **中国高校计算机大赛-网络技术挑战赛 (全国选拔赛)：三等奖** *省部级* 2024 &nbsp;&nbsp;[[证明]](..\docs\2024CCCCAxuanbasai.pdf)
- **“蓝桥杯”软件赛道 C++ 程序设计赛 (湖北赛区)：三等奖** *省部级* 2023 &nbsp;&nbsp;[[证明]](..\docs\lanqiaoshengsanC.png)

# 🥇 Scholarships and Honors

- *2023.10* **武汉大学甲等奖学金** (获奖率： 全校5%) *武汉大学* &nbsp;&nbsp;[[证明]](..\docs\23jiadeng.jpg)
- *2023.10* **三好学生** (获奖率： 全校10%) *武汉大学* &nbsp;&nbsp;[[证明]](..\docs\23sanhao.jpg)
- *2024.1* **武汉大学社会活动积极分子** *武汉大学国家网络安全学院* &nbsp;&nbsp;[[证明]](https://cse.whu.edu.cn/info/1100/22732.htm)

# 📖 Educations

- *2021.9 -*, 本科生, 武汉大学国家网络安全学院  专业： 信息安全.
