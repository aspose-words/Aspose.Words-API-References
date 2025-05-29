---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Margins 枚举，自定义文档边距。使用易于使用的预设增强您的文档格式！
type: docs
weight: 4580
url: /zh/net/aspose.words/margins/
---
## Margins enumeration

指定预设边距。

```csharp
public enum Margins
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Normal | `0` | 正常边距。 |
| Narrow | `1` | 边距较窄。 |
| Moderate | `2` | 中等利润。 |
| Wide | `3` | 边距较宽。 |
| Mirrored | `4` | 镜像边距。 |
| Custom | `5` | 自定义边距。 |

## 例子

显示何时重新计算文档的页面布局。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 将文档保存为 PDF、图像或首次打印时将自动
// 在文档的页面内缓存其布局。
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// 以某种方式修改文档。
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// 在当前版本的 Aspose.Words 中，修改文档不会自动重建
// 缓存的页面布局。如果我们希望使用缓存的布局
// 为了保持最新状态，我们需要手动更新它。
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
