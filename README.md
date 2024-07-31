![](https://s21.ax1x.com/2024/07/31/pkOjw24.png)

# PCL_Cat-DragonXAML(PCL首页随机暹罗猫&小恐龙表情包)📈
## 使用方法
1. ⌛打开PCL，在上方导航栏点击设置，左侧侧边栏点击个性化，找到“主页”这个板块，在“主页”板块点击“读取本地文件”，点击“生成教学文件”按钮，会提示生成文件，此时会打开一个文件夹，里面就有一个Custom.xaml
2. ⏳将Custom.xaml里的默认内容改为以下内容
```
<!-- 可以更改此处图片的API，以获取网上url图片 -->
<!-- 你也可以将暹罗猫的网址换成小恐龙的网址API，API如下：http://test1.ysone.top:56623/RI?type=KL -->

<local:MyCard Title="随机暹罗猫表情包" Margin="0,0,0,15">
    <StackPanel Margin="25,40,23,15">
        <Image Height="300" HorizontalAlignment="Center" Source="http://test1.ysone.top:56623/RI?type=LCat" />
        <local:MyHint Margin="0,8,0,2" IsWarn="False"
                    Text="需关掉重进PCL才刷新图片" />
        <Grid>
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="1*" />
                <ColumnDefinition Width="1.6*" MinWidth="200" /> <!-- 第二个按钮的宽度是第一个按钮的 1.6 倍，且至少为 200 -->
                <ColumnDefinition Width="150" /> <!-- 如果不打 *，则会占用固定的宽度，也可以写 Auto 来自适应 -->
            </Grid.ColumnDefinitions>
            <!-- 为按钮添加 Grid.Column 属性指定它所在的列，不要添加 Width 与 HorizontalAlignment 属性 -->
            <local:MyButton Grid.Column="0" Margin="0,0,10,0" Height="35" ColorType="Highlight"
                        Text="Github代码" EventType="打开网页" EventData="https://www.bilibili.com/" />
            <local:MyButton Grid.Column="1" Margin="0,0,10,0" Height="35" 
                        Text="关于作者" EventType="弹出窗口" EventData="关于作者|HantaFrog\nVer:0.1.5\n此项目属于开源项目，不属于任何商业项目\n感谢这位的API：\nhttp://test1.ysone.top/" />
        </Grid>
    </StackPanel>
</local:MyCard>
```
📦将以下代码复制到刚才生成的Custom.xaml，改完之后Ctrl+S保存文件，重启PCL

📥如果你把握不了复制的格式，也可以下载整个仓库，将原来的Custom.xaml文件删了，再将仓库里的cat&dragon.xaml改成Custom.xaml，重启PCL
