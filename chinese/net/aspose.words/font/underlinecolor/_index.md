---
title: Font.UnderlineColor
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 获取或设置应用于字体的下划线颜色
type: docs
weight: 540
url: /zh/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

获取或设置应用于字体的下划线颜色。

```csharp
public Color UnderlineColor { get; set; }
```

### 例子

显示如何配置文本下划线的样式和颜色。

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
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


