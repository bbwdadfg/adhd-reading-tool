# 🤝 贡献指南

感谢你对 ADHD Reading 项目的关注！我们欢迎所有形式的贡献，无论是代码、文档、设计还是用户反馈。这个项目的目标是帮助更多有阅读困难的用户，你的参与将让这个目标更快实现。

## 🌟 贡献方式

### 💻 代码贡献
- 修复 Bug 和问题
- 开发新功能
- 性能优化
- 代码重构

### 📝 文档贡献
- 改进用户文档
- 翻译多语言版本
- 编写教程和指南
- API 文档完善

### 🎨 设计贡献
- UI/UX 设计改进
- 图标和插画设计
- 用户体验优化
- 可访问性改进

### 🧪 测试贡献
- Bug 报告和复现
- 功能测试
- 兼容性测试
- 用户体验反馈

### 🌍 本地化贡献
- 界面翻译
- 文档翻译
- 本地化测试
- 文化适应性建议

## 🚀 快速开始

### 环境准备

1. **基础要求**
   ```bash
   Node.js >= 16.0.0
   npm >= 8.0.0
   Git >= 2.20.0
   ```

2. **开发工具推荐**
   - VS Code + 相关扩展
   - Chrome DevTools
   - Git 客户端

3. **Fork 和克隆项目**
   ```bash
   # Fork 项目到你的 GitHub 账户
   # 然后克隆到本地
   git clone https://github.com/your-username/adhd-reading.git
   cd adhd-reading
   ```

### 开发环境设置

1. **安装依赖**
   ```bash
   npm install
   ```

2. **开发模式运行**
   ```bash
   npm run dev
   ```

3. **加载到浏览器**
   - 打开 Chrome 扩展管理页面
   - 启用开发者模式
   - 加载 `dist` 目录

## 📋 开发规范

### 代码风格

**JavaScript/TypeScript**：
```javascript
// 使用 ES6+ 语法
const processText = (text, options = {}) => {
  // 函数命名使用驼峰式
  const { density = 0.4, strength = 1.2 } = options;

  // 使用 const/let，避免 var
  const words = text.split(' ');

  // 清晰的注释
  return words.map(word => {
    // 处理单词逻辑
    return emphasizeWord(word, density, strength);
  });
};
```

**CSS**：
```css
/* 使用 BEM 命名规范 */
.adhd-reading__container {
  /* 属性按字母顺序排列 */
  background-color: var(--bg-color);
  border-radius: 8px;
  padding: 16px;
}

.adhd-reading__button--active {
  background-color: var(--primary-color);
}
```

**HTML**：
```html
<!-- 语义化标签 -->
<section class="adhd-reading__settings">
  <h2 class="adhd-reading__title">设置选项</h2>

  <!-- 可访问性属性 -->
  <button
    class="adhd-reading__toggle"
    aria-label="启用仿生阅读"
    role="switch"
    aria-checked="false"
  >
    启用
  </button>
</section>
```

### 提交规范

使用 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

```bash
# 功能添加
git commit -m "feat: 添加语义高亮功能"

# Bug 修复
git commit -m "fix: 修复中文分词错误"

# 文档更新
git commit -m "docs: 更新安装指南"

# 样式调整
git commit -m "style: 调整按钮样式"

# 重构代码
git commit -m "refactor: 重构文本处理模块"

# 性能优化
git commit -m "perf: 优化大文本处理性能"

# 测试相关
git commit -m "test: 添加仿生阅读单元测试"
```

### 分支管理

```bash
# 主分支
main          # 稳定版本
develop       # 开发分支

# 功能分支
feature/semantic-highlighting
feature/dark-mode
feature/mobile-support

# 修复分支
fix/chinese-word-segmentation
fix/memory-leak

# 发布分支
release/v1.1.0
```

## 🐛 Bug 报告

### 报告模板

使用 GitHub Issues 报告 Bug，请包含以下信息：

```markdown
## Bug 描述
简洁清晰地描述遇到的问题

## 复现步骤
1. 打开网页 '...'
2. 点击 '...'
3. 滚动到 '...'
4. 看到错误

## 期望行为
描述你期望发生的情况

## 实际行为
描述实际发生的情况

## 环境信息
- 操作系统: [如 Windows 10]
- 浏览器: [如 Chrome 91.0.4472.124]
- 扩展版本: [如 1.0.1]
- 网站 URL: [如果相关]

## 截图
如果适用，添加截图帮助解释问题

## 附加信息
任何其他相关信息
```

### Bug 优先级

- **P0 - 紧急**: 导致扩展崩溃或无法使用
- **P1 - 高**: 核心功能异常
- **P2 - 中**: 次要功能问题
- **P3 - 低**: 界面或体验问题

## 💡 功能请求

### 请求模板

```markdown
## 功能描述
清晰描述你希望添加的功能

## 问题背景
这个功能解决什么问题？

## 解决方案
描述你希望的解决方案

## 替代方案
描述你考虑过的其他解决方案

## 用户价值
这个功能对用户有什么价值？

## 实现复杂度
你认为实现难度如何？（可选）
```

### 功能评估标准

- **用户价值**: 对 ADHD 用户的帮助程度
- **技术可行性**: 实现的技术难度
- **维护成本**: 长期维护的复杂度
- **兼容性影响**: 对现有功能的影响

## 🔄 Pull Request 流程

### 提交前检查

1. **代码质量**
   ```bash
   # 运行代码检查
   npm run lint

   # 运行测试
   npm run test

   # 构建检查
   npm run build
   ```

2. **功能测试**
   - 在多个网站测试功能
   - 验证不同语言的支持
   - 检查性能影响

3. **文档更新**
   - 更新相关文档
   - 添加使用示例
   - 更新 CHANGELOG

### PR 模板

```markdown
## 变更描述
简要描述这个 PR 的内容

## 变更类型
- [ ] Bug 修复
- [ ] 新功能
- [ ] 性能优化
- [ ] 文档更新
- [ ] 代码重构

## 测试
- [ ] 单元测试通过
- [ ] 手动测试完成
- [ ] 兼容性测试通过

## 截图
如果有 UI 变更，请提供截图

## 检查清单
- [ ] 代码遵循项目规范
- [ ] 自测试通过
- [ ] 文档已更新
- [ ] 无破坏性变更
```

### 代码审查

**审查要点**：
- 代码逻辑正确性
- 性能影响评估
- 安全性检查
- 可访问性验证
- 用户体验影响

**审查流程**：
1. 自动化检查通过
2. 至少一位维护者审查
3. 解决所有评论
4. 合并到主分支

## 🧪 测试指南

### 测试类型

**单元测试**：
```javascript
// 测试文本处理函数
describe('Text Processing', () => {
  test('should emphasize words correctly', () => {
    const input = 'Hello world';
    const result = emphasizeText(input, { density: 0.5 });
    expect(result).toContain('<strong>Hel</strong>lo');
  });
});
```

**集成测试**：
```javascript
// 测试扩展功能
describe('Extension Integration', () => {
  test('should apply bionic reading to page', async () => {
    await loadExtension();
    await navigateToPage('https://example.com');
    await enableBionicReading();

    const emphasizedElements = await findEmphasizedText();
    expect(emphasizedElements.length).toBeGreaterThan(0);
  });
});
```

**用户测试**：
- 可用性测试
- A/B 测试
- 用户反馈收集
- 长期使用跟踪

### 测试环境

**浏览器兼容性**：
- Chrome (最新版本 + 前两个版本)
- Edge (最新版本)
- Brave (最新版本)
- Opera (最新版本)

**操作系统**：
- Windows 10/11
- macOS 10.14+
- Ubuntu 20.04+

**网站类型**：
- 新闻网站
- 博客平台
- 学术网站
- 技术文档
- 社交媒体

## 🌍 国际化

### 翻译流程

1. **添加新语言**
   ```bash
   # 复制英文模板
   cp locales/en.json locales/zh-CN.json
   ```

2. **翻译文件格式**
   ```json
   {
     "appName": "ADHD Reading",
     "appSlogan": "优化阅读体验 · 提升专注力",
     "controls": {
       "enablePlugin": "启用插件",
       "autoApplySite": "自动应用此站点"
     }
   }
   ```

3. **翻译质量要求**
   - 准确传达原意
   - 符合本地化习惯
   - 保持术语一致性
   - 适当的文本长度

### 支持的语言

**当前支持**：
- 简体中文 (zh-CN)
- 繁体中文 (zh-TW)
- 英语 (en-US)
- 西班牙语 (es)
- 德语 (de)
- 法语 (fr)
- 阿拉伯语 (ar)
- 日语 (ja)
- 韩语 (ko)
- 葡萄牙语 (pt)

**计划支持**：
- 俄语 (ru)
- 意大利语 (it)
- 荷兰语 (nl)
- 印地语 (hi)

## 📞 联系方式

### 开发团队

- **项目维护者**: [GitHub @maintainer](https://github.com/maintainer)
- **技术负责人**: tech@adhdreading.org
- **设计负责人**: design@adhdreading.org

### 社区渠道

- **GitHub Discussions**: 技术讨论和问答
- **Discord 服务器**: 实时交流和协作
- **邮件列表**: 重要更新和公告
- **用户社区**: 用户反馈和建议

### 贡献者权益

**认可方式**：
- 贡献者列表展示
- 特殊徽章和标识
- 年度贡献者奖励
- 优先功能请求处理

**学习机会**：
- 代码审查反馈
- 技术分享会议
- 开源项目经验
- 简历项目展示

## 📜 行为准则

### 我们的承诺

我们致力于为每个人提供友好、安全和欢迎的环境，无论年龄、身体大小、残疾、种族、性别认同和表达、经验水平、教育程度、社会经济地位、国籍、个人外貌、种族、宗教或性取向如何。

### 我们的标准

**积极行为包括**：
- 使用友好和包容的语言
- 尊重不同的观点和经验
- 优雅地接受建设性批评
- 关注对社区最有利的事情
- 对其他社区成员表示同理心

**不可接受的行为包括**：
- 使用性化的语言或图像
- 恶意评论或人身攻击
- 公开或私下骚扰
- 未经许可发布他人私人信息
- 其他在专业环境中不当的行为

### 执行

项目维护者有权利和责任删除、编辑或拒绝不符合行为准则的评论、提交、代码、wiki 编辑、问题和其他贡献。

---

**感谢你的贡献！让我们一起为 ADHD 社区创造更好的阅读体验！** 🎉