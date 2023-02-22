---
title: LayoutOptions.IgnorePrinterMetrics
second_title: Aspose.Words for .NET API 参考
description: LayoutOptions 财产. 获取或设置是否忽略使用打印机度量来布局文档兼容性选项的指示 默认为 True
type: docs
weight: 50
url: /zh/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

获取或设置是否忽略“使用打印机度量来布局文档”兼容性选项的指示。 默认为 True。

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

### 例子

显示如何忽略“使用打印机指标来布置文档”选项。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### 也可以看看

* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../layoutoptions/)
* 部件 [Aspose.Words](../../../)


