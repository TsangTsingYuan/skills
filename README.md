# Skills

个人自用的 [Claude Code](https://claude.ai/code) skills 集合。

## 安装方式

将需要的 skill 目录复制或链接到 `~/.claude/skills/`：

```bash
# 方式一：复制
cp -r rd-doc-assistant ~/.claude/skills/

# 方式二：符号链接（便于后续更新）
ln -sf $(pwd)/rd-doc-assistant ~/.claude/skills/
```

重启 Claude Code 后即可使用。

## Skills 列表

### rd-doc-assistant

研发文档助手 - 中国标准研发流程的文档模板助手。

提供 7 个阶段、20 个文档模板的按需读取和内容填充，适用于 Web 应用、企业系统、移动应用等非嵌入式领域的研发文档编写。

- 需求调研与分析：需求文档、分析报告
- 立项：立项报告、项目计划书、预算方案
- 方案设计：技术方案文档、数据库设计、架构设计图
- 开发：源代码说明、单元测试报告、集成测试报告
- 测试与验证：测试报告、缺陷清单、验收报告
- 部署与发布：发布版本说明、用户手册、部署文档
- 维护与优化：优化报告、更新版本说明、维护记录
