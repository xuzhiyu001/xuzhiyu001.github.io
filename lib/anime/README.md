# Anime.js 配置

## 📦 版本
- **版本号:** 3.2.2
- **来源:** [juliangarnier/anime](https://github.com/juliangarnier/anime)
- **许可证:** MIT

## 📁 文件说明
- `anime.min.js` - 压缩版（生产环境使用）

## 🚀 使用方法

### 方法1: CDN引用
```html
<script src="https://xuzhiyu001.github.io/lib/anime/anime.min.js"></script>
```

### 方法2: 本地引用
```html
<script src="./lib/anime/anime.min.js"></script>
```

## 📝 示例代码

### 基础动画
```javascript
// 移动元素
anime({
  targets: '.box',
  translateX: 250,
  duration: 1000,
  easing: 'easeInOutQuad'
});

// 旋转 + 缩放
anime({
  targets: '.box',
  rotate: '1turn',
  scale: 1.5,
  duration: 2000
});

// 颜色动画
anime({
  targets: '.box',
  backgroundColor: '#FF6B6B',
  duration: 1000
});
```

### 关键帧动画
```javascript
anime({
  targets: '.box',
  keyframes: [
    { translateX: 0, translateY: 0 },
    { translateX: 100, translateY: -50 },
    { translateX: 200, translateY: 0 },
    { translateX: 100, translateY: 50 }
  ],
  duration: 2000
});
```

### 时间线
```javascript
const timeline = anime.timeline();

timeline.add({
  targets: '.box',
  translateX: 100,
  duration: 500
}).add({
  targets: '.box',
  rotate: 360,
  duration: 1000
}, '-=200'); // 相对于前一个动画-200ms开始
```

### 贝塞尔曲线
```javascript
anime({
  targets: '.box',
  translateX: 300,
  duration: 1000,
  easing: 'cubicBezier(0.175, 0.885, 0.32, 1.275)'
});
```

## 📚 更多资源
- 官方文档: https://animejs.com
- GitHub: https://github.com/juliangarnier/anime
- 示例: https://animejs.com/documentation/
