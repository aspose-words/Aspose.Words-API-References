---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words for .NET
description: 发现字体下划线颜色属性，轻松自定义字体的下划线颜色，以增强文本样式和视觉吸引力。
type: docs
weight: 550
url: /zh/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

获取或设置应用于字体的下划线的颜色。

```csharp
public Color UnderlineColor { get; set; }
```

## 例子

展示如何配置文本下划线的样式和颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
