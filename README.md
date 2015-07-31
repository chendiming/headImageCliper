# headImageCliper

`本组件已停止更新，请使用功能更丰富的组件`[imageCliper](https://github.com/libmw/imageCliper)


javascript头像裁剪上传组件，利用flash在本地进行裁剪后再上传，支持按尺寸预览头像，支持png、jpg、bmp、gif图片上传。

项目使用flashbuilder开发，可以用flashbuilder直接打开此项目。

![demo](http://libmw.github.io/resource/2015/headimagecliper/demo.png)

## 使用方法

1.把/bin-debug/headImageCliper.swf放到你的网站目录

2./demo文件夹下的所有图片和js放到你的网站目录。图片是swf文件需要使用的按钮、光标等，headImageCliper.js是与flash交互的组件HeadImageCliper。

3.使用如下代码调用裁剪组件：

```javascript
window.imageCliper = new HeadImageCliper({
    container: container, //上传界面的容器，原生dom
    flashUrl: '../bin-debug/headImageCliper.swf?v=0527', //上传flash的地址,加上版本号，防止flash被缓存
    width: container.clientWidth, //flash的宽度
    height: container.clientHeight, //flash的高度
    uploadUrl: 'upload.php', //上传路径
    file: 'file', //上传的字段名，默认为file
    isPreview: true, //是否显示预览图
    previewSize: '180|100|50', //预览图尺寸。'200|100'代表显示200*200和100*100的预览图。注意预览图的尺寸如果过大，可能会超出flash的可视范围，此时应该设置不显示预览图或者增大flash的宽高度
    resourceUrl: 'http://127.0.0.1/headImageCliper/demo/' //flash包含的按钮、光标等静态文件的放置路径
});
```

完整示例请[查看demo](http://libmw.github.io/2015/05/27/head-image-cliper.html)

有任何问题，mailto：libmw@163.com


