---
title: 更换登录页面UI
date: 2024-09-27 10:56:19
tags:
---
#### 1.创建组件
- 在component文件夹里新建一个ArkTS页面
![输入图片说明](https://foruda.gitee.com/images/1726822137906337277/26410929_14874948.png "屏幕截图")
- 在新建的页面输入用户登录界面代码

```
Column(){
      TextInput({placeholder: '账号'})
        .maxLength(20)
        .type(InputType.USER_NAME)
        .placeholderColor('#99182431')
        .height('48vp')
        .fontSize('18vp')
        .backgroundColor(Color.White)
        .width('100%')
        .padding({left:0})
        .margin({top:'12vp'})
      Line()
        .width('100%')
        .height('5vp')
        .backgroundColor('#0D182431')
      TextInput({placeholder: '密码'})
        .maxLength(20)
        .type(InputType.Password)
        .placeholderColor('#99182431')
        .height('48vp')
        .fontSize('18vp')
        .backgroundColor(Color.White)
        .width('100%')
        .padding({left:0})
        .margin({top:'12vp'})
    }
    .backgroundColor(Color.White)
    .borderRadius('24vp')
    .padding({top:'4vp',bottom:'4vp',left:'12vp',right:'12vp'})
```
