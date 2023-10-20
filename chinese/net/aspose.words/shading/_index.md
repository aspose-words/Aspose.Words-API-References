---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Shading 班级. 包含对象的着色属性 在 C#.
type: docs
weight: 5990
url: /zh/net/aspose.words/shading/
---
## Shading class

包含对象的着色属性。

```csharp
public class Shading : InternableComplexAttr
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | 获取或设置应用于 Shading 对象背景的颜色。 |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } |  |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } |  |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | 获取或设置应用于 Shading 对象前景的颜色。 |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } |  |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } |  |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | 获取或设置着色纹理。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | 移除对象的阴影。 |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | 确定指定对象的值是否与当前对象相等。 |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | 确定指定 Shading 的值是否与当前 Shading 相等。 |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | 用作此类型的散列函数。 |

## 例子

展示如何用边框和底纹装饰文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

展示如何在构建表格时应用边框和底纹颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启动一个表格并为其边框设置默认颜色/厚度。
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// 创建一个包含两个具有不同背景颜色的单元格的行。
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// 重置单元格格式以禁用背景颜色
// 为构建器创建的所有新单元格设置自定义边框粗细，
// 然后构建第二行。
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### 也可以看看

* class [InternableComplexAttr](../internablecomplexattr/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
