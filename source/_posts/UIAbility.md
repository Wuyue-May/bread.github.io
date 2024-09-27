---
title: 初始化UIAbility以及Text空间中文修改
date: 2024-09-27 10:54:08
tags:
---
### 相关概念

### 创建UIAbility组件
![输入图片说明](https://foruda.gitee.com/images/1725609476335112944/3980bb6d_14874948.png "屏幕截图")

### 创建编写Text组件
案例代码参考（将Text组件创建在build函数中，并且编写在Column之下）

```
build() {
    Column() {
      Text($r('app.string.hello_message'))
        .fontSize(CommonConstants.DEFAULT_FONT_SIZE)
        .fontColor(this.textColor)
        .margin(CommonConstants.DEFAULT_MARGIN)
        .fontWeight(FontWeight.Bold)
      Text($r('app.string.class_message'))
        .fontSize(CommonConstants.DEFAULT_FONT_SIZE)
        .fontColor(this.textColor)
        .margin(CommonConstants.DEFAULT_MARGIN)
        .fontWeight(FontWeight.Bold)
    }
    .width(CommonConstants.FULL_WIDTH)
  }
```

### 改写Text组件中的文字内容
主要操作：在resource文件夹下寻找对应的string.json同步改写改写其中的文字信息。
1. resources -> base -> element -> string.json
![输入图片说明](https://foruda.gitee.com/images/1725609835202287633/b5ebe93c_14874948.png "屏幕截图")
2. resources -> en-US -> element -> string.json
![输入图片说明](https://foruda.gitee.com/images/1725609852139674342/989c589b_14874948.png "屏幕截图")
3. resources -> zh-CN -> element -> string.json
![输入图片说明](https://foruda.gitee.com/images/1725609865737021543/1a1109d9_14874948.png "屏幕截图")

