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

要了解更多信息，请访问[使用文档编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class Shading : InternableComplexAttr
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | 获取或设置应用于背景的颜色`Shading`对象. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | 获取或设置与此关联的已应用配色方案中的背景图案主题颜色`Shading`对象. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | 获取或设置使背景主题颜色变亮或变暗的双精度值。 |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | 获取或设置应用于前景的颜色`Shading`对象. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | 获取或设置与此关联的已应用配色方案中的前景图案主题颜色`Shading`对象. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | 获取或设置一个双精度值，该值使前景色主题颜色变亮或变暗。 |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | 获取或设置着色纹理。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | 删除对象的阴影。 |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | 确定指定对象的值是否等于当前对象。 |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | 判断是否指定`Shading`与当前值相等`Shading`. |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | 用作该类型的哈希函数。 |

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

演示如何在构建表格时应用边框和底纹颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启动一个表格并为其边框设置默认颜色/厚度。
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// 创建一行，其中包含两个具有不同背景颜色的单元格。
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// 重置单元格格式以禁用背景颜色
// 为构建器创建的所有新单元格设置自定义边框厚度，
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
