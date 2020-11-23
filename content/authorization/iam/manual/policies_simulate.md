---
title: "策略模拟器"
date: 2020-02-28T10:08:56+09:00
description: 
draft: false
weight: 34
---

为了更好的让您迅速了解复杂策略的配置及多重叠加带来的权限影响，我们提供了**策略模拟器**。当您对策略叠加的预期评估结论产生疑问时，您可以使用策略模拟器获得准确的测试结论。

当新建自定义策略后，通过策略模拟器可以即时验证当前策略的权限配置，也可以在引用前随时对任意勾选的复合策略组合进行验证；

当身份附加策略后，策略模拟器可以验证多个合并的策略组合附加到身份是否符合预期，从而有效辅助您确认策略权限配置。

## 模拟入口

策略模拟器在 QingCloud 平台上作为一款可随时使用的工具，我们在任何需要的地方都提供呼出工具的入口。

### 单条策略模拟

您可以在策略列表点击鼠标右键，选择“策略模拟器”：

![图片](../../_images/ps1.png)

或在策略列表勾选当前策略，点击列表上方的“策略模拟器”：

![图片](../../_images/ps2.png)

### 任意复合策略组合模拟

与单条策略模拟类似，在策略列表勾选多条策略后点击“策略模拟器”即可。

### 身份上的策略权限验证

切换到身份列表点击鼠标右键，选择“策略模拟器”：

![图片](../../_images/ps12.png)

或进入任意策略详情查看策略引用，当存在引用的身份时，列表右侧将提供“模拟”链接：

![图片](../../_images/ps13.png)

## 模拟器的使用

### 模拟器布局

在弹出的策略模拟器窗口中，左侧将展示当前待测的所有策略并默认全部勾选，右侧提供使用者选择服务和待测操作。

![图片](../../_images/ps3.png)

当从身份上进入到策略模拟器时，左侧上方还将展示所选身份的信息，并可切换到其他支持模拟策略的身份上。

![图片](../../_images/ps14.png)

### 执行测试

依次选择好（身份和）策略、服务和操作后，点击“测试”即可完成当前复合的策略组合针对已选操作的初步模拟评估。

测试完后会将测试条目和测试结论针对性输出，如图所示：

![图片](../../_images/psa1.png)

如果用户配置了明确拒绝策略，支持点击后指引到对应的策略条目上：

![图片](../../_images/psa2.png)

整个操作过程中，您都可以在此处查看操作概览提示：

![图片](../../_images/ps4.png)

当您打算重新勾选的服务和操作时，您可以随时点击右侧的“清空”：

![图片](../../_images/ps11.png)

### 调整测试内容

1. 当您需要针对特定资源模拟操作时，可点击展开对应操作，使用[QRN生成器](../../faq/qrn#qrn生成器)来指定具体资源：

    ![图片](../../_images/ps5.png)

    > 了解更多关于 QRN 的信息，请点击：[资源标识符 QRN](../../faq/qrn)

2. 当您发现测试结论不符合预期时，还可以临时编辑调整策略后重新测试。鼠标移到某条策略上后点击右侧的“编辑”：

    ![图片](../../_images/ps9.png)

    调整对应策略内容后点击“保存”：

    ![图片](../../_images/ps10.png)

若您已经在当前模拟器执行过“测试”，再调整测试内容会使得测试结论不再有效。我们会提醒您需要重新执行测试：

![图片](../../_images/ps8.png)

再次执行测试后，将会生成最新的模拟结果。