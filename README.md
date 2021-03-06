# live2d前端看板娘

静态的看板娘是只有一个模型，换模型需修改代码并刷新页面

动态的看板娘可以和用户互动，不刷新页面换模型，换衣等操作


## 静态看板娘
源代码如下：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>小萝莉模型</title>
</head>

<body>
    <script src="https://eqcn.ajz.miesnfu.com/wp-content/plugins/wp-3d-pony/live2dw/lib/L2Dwidget.min.js"></script>
    <script>
        L2Dwidget.init({
            "model": {　 //jsonpath控制显示那个小萝莉模型，
                //(切换模型需要改动)
                jsonPath: "https://unpkg.com/live2d-widget-model-miku@1.0.5/assets/miku.model.json",
                /*
                其他可选的模型：
                黑猫：https://unpkg.com/live2d-widget-model-hijiki@1.0.5/assets/hijiki.model.json
                萌娘：https://unpkg.com/live2d-widget-model-shizuku@1.0.5/assets/shizuku.model.json
                白猫：https://unpkg.com/live2d-widget-model-tororo@1.0.5/assets/tororo.model.json
                狗狗：https://unpkg.com/live2d-widget-model-wanko@1.0.5/assets/wanko.model.json
                小可爱：https://unpkg.com/live2d-widget-model-z16@1.0.5/assets/z16.model.json
                小可爱：https://unpkg.com/live2d-widget-model-koharu@1.0.5/assets/koharu.model.json
                ...
                */
                "scale": 1
            },
            "display": {
                "position": "right", //看板娘的表现位置
                "width": 150, //小萝莉的宽度
                "height": 300, //小萝莉的高度
                "hOffset": 0,
                "vOffset": -20
            },
            "mobile": {
                "show": true,
                "scale": 0.5
            },
            "react": {
                "opacityDefault": 0.7,
                "opacityOnHover": 0.2
            }
        });
    </script>
</body>

</html>
```
更多模型请访问
模型网址和预览：
https://huaji8.top/post/live2d-plugin-2.0/
只需将模型名字，替换模型url的花括号即可
https://unpkg.com/live2d-widget-model-{}@1.0.5/assets/{}.model.json


## 动态看板娘

\# server.html --> 直接调用即可,资源在网络端，需要联网

\# client.html --> 把资源文件全部下载在live2d-weight文件夹中，可以在断网的情况下观看

源码如下
```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8">
    <title></title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/font-awesome/css/font-awesome.min.css">
</head>

<body>
    <script src="https://cdn.jsdelivr.net/gh/stevenjoezhang/live2d-widget/autoload.js"></script>
</body>

</html>
```




## 参考博客
曳猫：https://blog.csdn.net/weixin_45936690/article/details/103989848

live2d-weight 源码：https://github.com/stevenjoezhang/live2d-widget
