---
name: rd-doc-assistant
description: >
  研发文档助手 - 中国标准研发流程的文档模板助手。
  当用户需要编写通用研发文档（需求文档、技术方案、项目计划书、数据库设计、
  测试报告、验收报告、缺陷清单、部署文档、用户手册、维护记录等）时激活。
  适用于Web应用、企业系统、移动应用等非嵌入式领域的研发项目。
  【注意】不处理STM32/单片机/嵌入式/固件相关文档——那些由embedded-systems skill处理。
  按7阶段流程提供对应模板并协助填充内容。
keywords: 文档, 研发, 需求, 方案, 测试, 部署, 维护, 模板, 报告, 立项, 验收, 设计文档
license: MIT
metadata:
  version: "1.0.0"
  domain: general
  role: assistant
  scope: documentation
  output-format: document
  related-skills:
    - embedded-systems
---

# 研发文档助手

中国标准研发流程的文档模板助手。提供7个阶段、20个文档模板的按需读取和内容填充。

## 模板文件位置

所有模板位于 skill 目录的相对路径下：
- 模板：`references/templates/`
- 参考指南：`references/研发流程.md`
- 设计方案框架：`references/设计方案标准框架指南.md`

## 7阶段研发流程

| 阶段 | 目标 | 产出文档 |
|------|------|---------|
| 1. 需求调研与分析 | 明确研发需求，确定项目方向和目标 | 需求文档、需求分析报告 |
| 2. 立项 | 正式批准项目启动，明确范围/预算/资源 | 立项报告、项目计划书、预算方案 |
| 3. 方案设计 | 制定技术方案和架构，为开发提供指导 | 技术方案文档、数据库设计、架构设计图 |
| 4. 开发 | 将设计方案转化为实际产品/系统 | 源代码说明、单元测试报告、集成测试报告 |
| 5. 测试与验证 | 验证功能/性能/可靠性是否符合要求 | 测试报告、缺陷清单、验收报告 |
| 6. 部署与发布 | 部署到生产环境供用户使用 | 发布版本说明、用户手册、部署文档 |
| 7. 维护与优化 | 持续维护产品，优化性能和功能 | 优化报告、更新版本说明、维护记录 |

## 模板索引

### Phase 1 — 需求调研与分析
- `references/templates/01-需求分析报告.md`
- `references/templates/01-需求文档.md`

### Phase 2 — 立项
- `references/templates/02-立项报告.md`
- `references/templates/02-项目计划书.md`
- `references/templates/02-预算方案.md`

### Phase 3 — 方案设计
- `references/templates/03-技术方案文档.md`
- `references/templates/03-数据库设计文档.md`
- `references/templates/03-架构设计图.md`

### Phase 4 — 开发
- `references/templates/04-源代码说明.md`
- `references/templates/04-单元测试报告.md`
- `references/templates/04-集成测试报告.md`

### Phase 5 — 测试与验证
- `references/templates/05-测试报告.md`
- `references/templates/05-缺陷清单.md`
- `references/templates/05-验收报告.md`

### Phase 6 — 部署与发布
- `references/templates/06-发布版本说明.md`
- `references/templates/06-用户手册.md`
- `references/templates/06-部署文档.md`

### Phase 7 — 维护与优化
- `references/templates/07-优化报告.md`
- `references/templates/07-更新版本说明.md`
- `references/templates/07-维护记录.md`

## 工作流程

1. **判断请求类型**：如果请求涉及STM32/单片机/嵌入式/固件/RTOS相关文档编写，**跳过**让embedded-systems skill处理
2. **确定阶段**：根据用户需求判断属于哪个研发阶段
3. **读取模板**：从 `references/templates/` 读取对应模板
4. **填充内容**：使用用户提供的项目信息，替换模板中的 `[占位符]` 和 `<!-- 注释 -->`
5. **参考框架**：编写技术方案时，按需读取 `references/设计方案标准框架指南.md` 补充框架指导
6. **输出完整文档**：输出填充后的完整文档，保留模板的版本历史结构

## 模板统一结构说明

所有模板遵循相同模式：
- 文档信息表（项目名称、版本、日期、作者）
- 分章节内容（每章含表格或列表占位符）
- HTML注释作为编写指引
- 末尾版本历史表

## 注意事项

- 使用用户的项目上下文填充占位符，不要保留 `[占位符]` 原文
- HTML注释 `<!-- ... -->` 应根据实际内容替换或删除
- 保留模板的表格格式和结构一致性
- 输出前检查是否有遗漏的未填充占位符
