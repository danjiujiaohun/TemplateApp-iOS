# TemplateApp-iOS
这个为iOS开发初始模版，已创建好BaseViewController、UIColor、UIImage等快捷方法架构
在新建新App时可直接拉取使用，仅需更改相关App名称即可。
在App文件和配置文件等信息需更改名称，注：podfile文件中也需要更改App名称
## 最好的使用方式：
1.自己创建自己想要开发的App项目
2.git clone该项目
3.将UIColor、UIImage、RootViewController等文件复制进新的项目中
4.创建BaseUnit文件夹，复制文件下相关代码到新项目中
5.更改Assets、Info文件内容为模板项目文件内容
6.修改podfile中App名称
7.在终端执行pod install指令

#### BaseViewController
1.使用方式：
控制器继承BaseViewController类
2.主要优势：
可以使用setBarButtonItem方法快捷创建控制器的NavigationBar的图标，并且可以通过leftItemAction、rightItemAction等方式实现点击时间

#### UIColor快捷使用方式
1.创建新颜色：
  a.在Assets中的UIColor文件夹下新增一个新颜色，以color_xxxxxx(xxxxxx为颜色的16进制编码)
  b.在UIColor中新增枚举类型，新增刚刚新增的颜色
2.快捷使用颜色：
使用UIColor.color(.color_xxxxxx)方法进行使用对应颜色，例如纯白色：UIColor.color(.color_FFFFFF)

#### UIImage快捷使用方式
1.新增新图片：
  a.将图片命名为：image_xxxx的命名方式，并拖入Assets中的UIImage文件夹下。
  b.在UIImage文件中新增枚举类型，新增刚刚的图片文件名称，枚举值为图片名称去除image_部分
2.快捷使用图片
使用UIImage.image(.xxxx)方法进行使用对应图片，例如返回图标：UIImage.smart(.back_icon)

#### 模版中仍有一些快捷方式可供大家使用，大家可以简单查看BaseUnit文件中的内容，以下做每个文件的简单介绍：
1.AdapterExt -> 屏幕宽高比例适配方式
2.BaseViewController -> 基础控制器类
3.Common -> 屏幕通用宽高、导航栏高度等信息
4.UIFontExt -> UIFont字体的快捷使用方法，常用使用方法： UIFont.font(of: CGFloat, weight: ZUFontWeight)，举例：UIFont.font(of: 12.fit(), weight: .regular)
5.UILabelExt -> UILabel的快捷使用方法，常用使用方法：UILabel.label(text: String, textColor: UIColor, font: UIFont), 举例：UILabel.label("text", textColor: UIColor.color(.color_000000), font: UIFont.font(of: 12.fit(), weight: .regular))

###### 如有相关问题或建议，欢迎大家提issues
