---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: 用于 .NET 的 Aspose.Words
description: LayoutOptions IgnorePrinterMetrics 财产. 获取或设置是否忽略使用打印机指标来设计文档布局兼容性选项的指示 默认为真的 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

获取或设置是否忽略“使用打印机指标来设计文档布局”兼容性选项的指示。 默认为`真的`.

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## 例子

演示如何忽略“使用打印机指标来设计文档布局”选项。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### 也可以看看

* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
