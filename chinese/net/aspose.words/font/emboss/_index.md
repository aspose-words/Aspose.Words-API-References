---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: 用于 .NET 的 Aspose.Words
description: Font Emboss 财产. 如果字体格式为浮雕则为 True 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words/font/emboss/
---
## Font.Emboss property

如果字体格式为浮雕，则为 True。

```csharp
public bool Emboss { get; set; }
```

## 例子

展示如何对文本应用雕刻/浮雕效果。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// 下面是使用阴影对文本应用类似 3D 效果的两种方法。
// 1 - 雕刻文本，使其看起来像是字母凹陷到页面中：
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - 浮雕文本，使其看起来像是字母从页面中弹出：
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
