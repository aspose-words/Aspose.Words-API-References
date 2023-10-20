---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: 用于 .NET 的 Aspose.Words
description: Font Shadow 财产. 如果字体格式为阴影则为 True 在 C#.
type: docs
weight: 330
url: /zh/net/aspose.words/font/shadow/
---
## Font.Shadow property

如果字体格式为阴影，则为 True。

```csharp
public bool Shadow { get; set; }
```

## 例子

演示如何创建带有阴影格式的文本串。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置阴影标志以应用偏移阴影效果，
// 使字母看起来像是漂浮在页面上方。
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
