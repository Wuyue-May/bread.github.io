---
title: 项目组件规划
date: 2024-09-27 10:55:35
tags:
---
## 项目目录规划
随着项目的不断演进，代码、组件、图示会不断增多，如果都填写在同一个文件中，不利于代码阅读和维护，更不利于开发，为此我们将项目中的子组件从一个文件中拆分出来。

- component文件夹 -> 存放组件代码
- model文件夹 -> 存放类代码
- page文件夹 -> 存放页面代码
- view文件夹 -> 存放视图代码
![输入图片说明](https://foruda.gitee.com/images/1726218229485188154/17c3cb31_14874948.png "屏幕截图")
## 子组件的编写
项目中常用用的视图，我们会将这些小组件组合编写成自定义组件。如果是更大的视图（会重复用到的），我们会编写成视图，方便调用。
- 例如：我们将轮播图单独归纳成为一个组件，并创建单独的Arkts文件存放，保存在component文件夹中。
![输入图片说明](https://foruda.gitee.com/images/1726218366947827266/915733d7_14874948.png "屏幕截图")


```
import { BannerClass } from '../model/BannerClass';

@Component
export  struct Banner {
  @State bannerList:Array<BannerClass> = [
    new BannerClass('pic0',$r('app.media.banner_pic0'),''),
    new BannerClass('pic1',$r('app.media.banner_pic1'),''),
    new BannerClass('pic2',$r('app.media.banner_pic2'),''),
    new BannerClass('pic3',$r('app.media.banner_pic3'),''),
    new BannerClass('pic4',$r('app.media.banner_pic4'),''),
    new BannerClass('pic5',$r('app.media.banner_pic5'),'')
  ];
  build() {
    Swiper() {
      ForEach(this.bannerList,(item:BannerClass,index:number)=>{
        Image(item.imageSrc)
          .objectFit(ImageFit.Contain)
          .width('100%')
          .padding({top:11,left:16,right:36})
          .borderRadius(16)
      },(item:BannerClass,index:number)=> item.id)
    }
    .autoPlay(true)
    .loop(true)
    .indicator(
      new DotIndicator()
        .color('#1a000000')
        .selectedColor('8A59F7')
    )
  }
}
```
##### 注意：子组件需要在其他文件中引用，我们要写上export语句，以便使用的文件可以通过import导入。
- 组件导入时使用import语句，例如：import { Banner } from '../component/Banner'
注意组件名称这里要加大括号{}。