---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: 用于 .NET 的 Aspose.Words
description: Font ComplexScript 财产. 指定在确定此运行的格式时是否应将此运行的内容视为复杂脚本文本而不管 它们的 Unicode 字符值 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

指定在确定此运行的格式时，是否应将此运行的内容视为复杂脚本文本，而不管 它们的 Unicode 字符值。

```csharp
public bool ComplexScript { get; set; }
```

## 例子

演示如何添加始终被视为复杂脚本的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
