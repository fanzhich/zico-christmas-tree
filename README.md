# Zico Christmas Tree · HTML / WebGL 版

这是将 [ZekangLi-Zico / Christmas-Tree](https://github.com/ZekangLi-Zico/Christmas-Tree) 的 Python + Pygame 粒子动画迁移后的浏览器版本。

## 打开方式

直接双击 `index.html` 即可，整个页面只有一个文件，不需要安装 Python、Pygame 或任何前端依赖，也可以离线运行。

如果希望用本地服务器打开：

```powershell
python -m http.server 4173
```

然后访问 `http://127.0.0.1:4173/`。

## 个性化

原项目中的 `647` 已保留为默认署名。可以在网址后添加 `name` 参数换成自己的名字：

```text
index.html?name=YOUR_NAME
```

中文名字可以先做 URL 编码，例如 `小明` 可写成 `%E5%B0%8F%E6%98%8E`。

## 操作

- 拖动画面：手动旋转圣诞树
- 空格键或暂停按钮：暂停 / 继续
- `F`、全屏按钮或双击画面：进入 / 退出全屏

## 实现说明

- 使用原生 WebGL 一次绘制约 56,200 个粒子，没有 Three.js 等外部运行时
- 保留原项目的 50,000 个树体点、4,000 个地面光环点、1,200 个星点、1,000 个树顶爱心点和 10 片前景大雪花
- 使用深度遮挡与径向光晕还原 Pygame 版的冷色粒子效果
- 自适应桌面、平板与手机尺寸，并支持系统“减少动态效果”设置
- 不收集数据，不需要网络请求

原项目版权与署名归其作者所有；本项目页面在保留视觉算法特征的基础上补充了网页交互和响应式排版。
