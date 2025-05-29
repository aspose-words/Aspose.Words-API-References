---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words for .NET
description: 探索 Font TextEffect 属性，轻松自定义字体动画，通过动态文本效果增强您的设计，带来迷人的用户体验。
type: docs
weight: 460
url: /zh/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

获取或设置字体动画效果。

```csharp
public TextEffect TextEffect { get; set; }
```

## 例子

展示如何将视觉效果应用于运行。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// 旧版本的 Microsoft Word 仅支持字体动画效果。
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### 也可以看看

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
