---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words for .NET
description: 探索“字体轮廓”属性。轻松将字体格式化为轮廓，打造独特的设计风格。使用这个简单的功能，提升您的排版效果！
type: docs
weight: 300
url: /zh/net/aspose.words/font/outline/
---
## Font.Outline property

如果字体格式为轮廓，则为真。

```csharp
public bool Outline { get; set; }
```

## 例子

展示如何创建格式化为大纲的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置轮廓标志以将文本的填充颜色更改为白色，并且
// 在文本的原始颜色中在每个字符周围留下细轮廓。
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
