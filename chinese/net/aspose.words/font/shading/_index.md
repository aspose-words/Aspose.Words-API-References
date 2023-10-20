---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: 用于 .NET 的 Aspose.Words
description: Font Shading 财产. 返回一个Shading引用字体阴影格式的对象 在 C#.
type: docs
weight: 320
url: /zh/net/aspose.words/font/shading/
---
## Font.Shading property

返回一个[`Shading`](../../shading/)引用字体阴影格式的对象。

```csharp
public Shading Shading { get; }
```

## 例子

演示如何将底纹应用于文档生成器创建的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// 使使用白色字体颜色创建的文本可见的一种方法
// 是应用背景阴影效果。
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### 也可以看看

* class [Shading](../../shading/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
