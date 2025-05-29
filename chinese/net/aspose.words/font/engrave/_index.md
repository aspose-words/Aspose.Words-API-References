---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words for .NET
description: 探索字体雕刻功能。轻松格式化字体，打造优雅的雕刻效果，提升设计的精致感和吸引力。
type: docs
weight: 120
url: /zh/net/aspose.words/font/engrave/
---
## Font.Engrave property

如果字体格式为雕刻，则为真。

```csharp
public bool Engrave { get; set; }
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
