---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words for .NET
description: 探索 Font TintAndShade 属性，轻松调整颜色！亮化或暗化阴影，打造活力四射的设计。轻松提升您的项目！
type: docs
weight: 530
url: /zh/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

获取或设置使颜色变亮或变暗的双精度值。

```csharp
public double TintAndShade { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 如果将此属性设置为小于 -1 或大于 1 的值，则抛出。 |
| InvalidOperationException | 如果设置此属性为[`Font`](../)具有非主题颜色的对象。 |

## 评论

此属性的允许值范围是从 -1（最暗）到 1（最亮）。

零（0）是中性的。

## 例子

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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
