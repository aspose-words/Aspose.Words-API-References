---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: 用于 .NET 的 Aspose.Words
description: Font Italic 财产. 如果字体格式为斜体则为 True 在 C#.
type: docs
weight: 160
url: /zh/net/aspose.words/font/italic/
---
## Font.Italic property

如果字体格式为斜体，则为 True。

```csharp
public bool Italic { get; set; }
```

## 例子

演示如何使用文档生成器编写斜体文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
