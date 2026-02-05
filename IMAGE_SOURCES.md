# 图片源配置说明

## 当前状态
如果您的 GitHub 主页上只有部分图片能显示，这是因为这些免费服务经常不稳定。

## 快速修复方法

### 方法 1: 等待恢复（推荐）
这些服务通常会在几小时内自动恢复。刷新页面时按 `Ctrl + Shift + R` 强制清除缓存。

### 方法 2: 手动切换备用源
打开 `README.md`，找到对应的图片部分，按照注释说明取消注释备用源。

## 各个组件的备用源

### 1. Typing SVG（动画标题）

**主源**:
```markdown
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=32&duration=2800&pause=2000&color=A9FEF7&center=true&vCenter=true&width=940&lines=Hi+%F0%9F%91%8B+I'm+jengzang;HITSZ+Student+%7C+Full+Stack+Developer;Dialect+Enthusiast;Always+learning+new+things!" alt="Typing SVG" />
```

**备用源 1** (Herokuapp):
```markdown
<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=32&duration=2800&pause=2000&color=A9FEF7&center=true&vCenter=true&width=940&lines=Hi+%F0%9F%91%8B+I'm+jengzang;HITSZ+Student+%7C+Full+Stack+Developer" alt="Typing SVG" />
```

**备用源 2** (简化版):
```markdown
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=32&color=A9FEF7&center=true&vCenter=true&width=940&lines=Hi+I'm+jengzang;Full+Stack+Developer" alt="Typing SVG" />
```

### 2. GitHub Stats Card（统计卡片）

**主源**:
```markdown
https://github-readme-stats-sigma-five.vercel.app/api?username=jengzang&show_icons=true&theme=radical&include_all_commits=true&count_private=true&cache_seconds=86400
```

**备用源 1** (官方):
```markdown
https://github-readme-stats.vercel.app/api?username=jengzang&show_icons=true&theme=radical&include_all_commits=true&count_private=true
```

**备用源 2** (Rickstaa):
```markdown
https://github-readme-stats-git-masterrstaa-rickstaa.vercel.app/api?username=jengzang&show_icons=true&theme=radical
```

**备用源 3** (自定义实例):
```markdown
https://github-readme-stats-one-bice.vercel.app/api?username=jengzang&show_icons=true&theme=radical
```

### 3. Streak Stats（连续贡献）

**主源**:
```markdown
https://streak-stats.demolab.com/?user=jengzang&theme=radical&date_format=M%20j%5B%2C%20Y%5D&cache_seconds=86400
```

**备用源 1** (Herokuapp - 可能已停用):
```markdown
https://github-readme-streak-stats.herokuapp.com/?user=jengzang&theme=radical
```

**备用源 2** (DenverCoder1):
```markdown
https://streak-stats.demolab.com/?user=jengzang&theme=radical
```

### 4. Language Stats（语言统计）

**主源**:
```markdown
https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=jengzang&layout=compact&theme=radical&langs_count=8&cache_seconds=86400
```

**备用源 1** (官方):
```markdown
https://github-readme-stats.vercel.app/api/top-langs/?username=jengzang&layout=compact&theme=radical&langs_count=8
```

**备用源 2** (不同布局):
```markdown
https://github-readme-stats.vercel.app/api/top-langs/?username=jengzang&layout=donut&theme=radical
```

### 5. Trophy（成就徽章）

**主源**:
```markdown
https://github-profile-trophy.vercel.app/?username=jengzang&theme=radical&column=4&margin-w=15&margin-h=15&no-frame=true
```

**备用源 1** (不同列数):
```markdown
https://github-profile-trophy.vercel.app/?username=jengzang&theme=radical&column=3&row=2
```

**备用源 2** (简化版):
```markdown
https://github-profile-trophy.vercel.app/?username=jengzang&theme=radical
```

### 6. Activity Graph（活动图表）

**主源**:
```markdown
https://github-readme-activity-graph.vercel.app/graph?username=jengzang&theme=react-dark&hide_border=true&area=true
```

**备用源 1** (不同主题):
```markdown
https://github-readme-activity-graph.vercel.app/graph?username=jengzang&theme=github-compact
```

**备用源 2** (Ashutosh00710):
```markdown
https://activity-graph.herokuapp.com/graph?username=jengzang&theme=react-dark
```

## 自动化解决方案（高级）

### 选项 1: 部署自己的实例
您可以 fork 这些项目并部署到自己的 Vercel 账号：
- GitHub Stats: https://github.com/anuraghazra/github-readme-stats
- Streak Stats: https://github.com/DenverCoder1/github-readme-streak-stats
- Trophy: https://github.com/ryo-ma/github-profile-trophy

### 选项 2: 使用 GitHub Actions 定期检查
创建一个 GitHub Action 定期检查哪些源可用，自动更新 README。

### 选项 3: 使用图片代理服务
使用 Cloudflare Workers 或其他代理服务，自动尝试多个源。

## 常见问题

### Q: 为什么图片加载很慢？
A: 这些服务需要实时从 GitHub API 获取数据并生成图片，第一次加载会比较慢。添加 `cache_seconds` 参数可以改善。

### Q: 为什么有些图片显示 "503 Service Unavailable"？
A: 这些免费服务有流量限制，高峰期可能无法访问。等待几小时后通常会恢复。

### Q: 如何知道哪个源可用？
A: 直接在浏览器中打开图片 URL，如果能看到图片就说明可用。

### Q: 可以同时使用多个源吗？
A: 不建议。GitHub Markdown 不支持自动 fallback，同时加载多个源会增加加载时间。

## 推荐配置

根据稳定性，推荐使用以下组合：

1. **最稳定**（功能较少）:
   - Stats: 官方 vercel.app
   - Streak: demolab.com
   - 去掉 Trophy 和复杂参数

2. **平衡**（当前配置）:
   - Stats: sigma-five.vercel.app
   - Streak: demolab.com
   - Trophy: 官方
   - 添加 cache_seconds

3. **功能最全**（可能不稳定）:
   - 所有组件都启用
   - 使用所有高级参数
   - 需要经常检查和切换源

## 更新日志

- 2026-02-05: 初始配置，添加多个备用源
- 修复 Typing SVG 中文字符编码问题
- 添加缓存参数提高稳定性
