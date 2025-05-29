---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: Aspose.Words for .NET
description: 探索“字体浮雕”属性，为您的文字增添时尚的浮雕效果，打造引人注目的设计。立即提升您的排版效果！
type: docs
weight: 100
url: /zh/net/aspose.words/font/emboss/
---
## Font.Emboss property

如果字体格式为浮雕，则为真。

```csharp
public bool Emboss { get; set; }
```

## 例子

展示如何将雕刻/浮雕效果应用于文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// 以下是两种使用阴影为文本应用 3D 效果的方法。
// 1 - 雕刻文字，使字母看起来像是沉入页面中：
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - 浮雕文本，使其看起来像字母从页面中弹出：
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
