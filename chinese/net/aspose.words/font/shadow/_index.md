---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words for .NET
description: 发现字体阴影属性，使用时尚的阴影效果增强您的文本，使您的设计具有引人注目的视觉吸引力。
type: docs
weight: 340
url: /zh/net/aspose.words/font/shadow/
---
## Font.Shadow property

如果字体格式为阴影，则为真。

```csharp
public bool Shadow { get; set; }
```

## 例子

展示如何创建带有阴影格式的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置阴影标志以应用偏移阴影效果，
// 使字母看起来就像漂浮在页面上方。
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
