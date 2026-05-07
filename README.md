# Skills

个人自用的 [Claude Code](https://claude.ai/code) skills 集合。

## 安装方式

将需要的 skill 目录复制或链接到 `~/.claude/skills/`：

```bash
# 方式一：复制所有 skills
cp -r * ~/.claude/skills/

# 方式二：符号链接整个仓库（便于后续更新）
ln -sfT $(pwd) ~/.claude/skills
```

重启 Claude Code 后即可使用。

## Skills 列表

### rd-doc-assistant

研发文档助手 - 中国标准研发流程的文档模板助手。提供 7 个阶段、20 个文档模板的按需读取和内容填充。

### embedded-systems

嵌入式系统工程师 skill - 精通微控制器编程、RTOS 实现、硬件-软件集成。适用于 STM32、ESP32、FreeRTOS、裸机开发、功耗优化等场景。

### skill-creator

创建、修改和优化 Claude Code skills 的工具。支持从零创建 skill、编辑现有 skill、运行 eval 测试、优化 description 触发准确性。

### find-skills

帮助发现和安装 Claude Code agent skills。通过 `npx skills` CLI 搜索和安装社区 skills。

### word-optimizer

专业文本润色和优化工具。优化中文/英文表达、精简冗余内容、统一文档风格、润色邮件报告等。
