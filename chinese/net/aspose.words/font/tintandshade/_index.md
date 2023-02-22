---
title: Font.TintAndShade
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 获取或设置使颜色变亮或变暗的双精度值
type: docs
weight: 520
url: /zh/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

获取或设置使颜色变亮或变暗的双精度值。

```csharp
public double TintAndShade { get; set; }
```

### 评论

此属性的允许值范围为 -1（最暗）到 1（最亮）。 零 (0) 表示中性。尝试将此属性设置为小于 -1 或大于 1 的值会导致ArgumentOutOfRangeException.

为具有非主题颜色 的字体对象设置此属性会导致InvalidOperationException.

### 例子

展示如何创建和使用主题风格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// 使用主题字体属性创建一些样式。
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


