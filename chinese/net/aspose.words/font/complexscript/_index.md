---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words for .NET
description: 发现字体 ComplexScript 属性，确保您的文本格式化为复杂脚本，以增强可读性和样式，而不管 Unicode 值如何。
type: docs
weight: 80
url: /zh/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

指定在确定此运行的格式时，是否应将此运行的内容视为复杂脚本文本，而不管其 Unicode 字符值如何。

```csharp
public bool ComplexScript { get; set; }
```

## 例子

展示如何添加始终被视为复杂脚本的文本。

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
