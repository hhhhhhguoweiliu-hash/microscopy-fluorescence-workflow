# Microscopy Fluorescence Workflow

一套可复用的显微图像红色荧光分析规范，覆盖：

- Leica LIF/TIFF 文件检查；
- ICC与原始图、10×与20×图像整理；
- ImageJ红色通道平均荧光强度批量测量；
- Excel速查表和Prism数据格式；
- 图片编号、定量数据与PPT图片的一致性管理；
- 自动执行、用户确认和科学讨论的边界。

## 内容

- [完整中文工作流](WORKFLOW.md)
- [Codex skill](skills/microscopy-fluorescence-workflow/SKILL.md)
- [详细操作流程](skills/microscopy-fluorescence-workflow/references/workflow.md)
- [确认与讨论边界](skills/microscopy-fluorescence-workflow/references/decision-boundaries.md)

## 使用skill

将 `skills/microscopy-fluorescence-workflow` 复制到 Codex skills 目录，然后使用：

```text
$microscopy-fluorescence-workflow
```

示例：

```text
使用 $microscopy-fluorescence-workflow 检查这批ICC图像，计算红色通道平均荧光强度，
整理成Prism格式，并按最终速查表制作PPT。
```

skill会优先建立来源、通道、分组边界、筛选规则和输出格式的数据契约，并在可能改变实验结论或破坏原始数据的节点请求用户确认。
