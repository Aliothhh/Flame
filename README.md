# 《爝火不熄》GitHub Pages 发布包

## 发布

1. 在 GitHub 新建一个 **Public** 仓库。
2. 解压本压缩包，把 `index.html`、`assets` 文件夹和本说明一起上传到仓库根目录。
3. 打开仓库 `Settings → Pages`。
4. 在 `Build and deployment` 中选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/ (root)`，点击 `Save`。
6. 等待约一至数分钟，GitHub 会显示公开网址。

不要只上传 `index.html`；图片、音乐、字体和剧情数据均在 `assets` 中。

## 结局数据统计（可选）

页面已经预留 Supabase 写入接口。在 `index.html` 最后一个主脚本之前加入：

```html
<script>
window.JUEHUO_STATS = {
  url: "https://你的项目.supabase.co",
  key: "你的 publishable key"
};
</script>
```

不填写时不影响游戏，只是不记录结局数据。严禁在网页中填写 `service_role` 密钥。
