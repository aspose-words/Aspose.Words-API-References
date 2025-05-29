---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words for .NET
description: 探索 LayoutOptions 的 IgnorePrinterMetrics 属性，控制文档布局的打印机指标。优化兼容性并提升打印精度。
type: docs
weight: 50
url: /zh/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

获取或设置是否忽略“使用打印机指标来布局文档”兼容性选项的指示。 默认值为`真的`.

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## 例子

显示如何忽略“使用打印机指标来布局文档”选项。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### 也可以看看

* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
