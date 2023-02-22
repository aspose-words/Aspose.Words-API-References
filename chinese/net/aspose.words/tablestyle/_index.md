---
title: Class TableStyle
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.TableStyle 班级. 表示表格样式
type: docs
weight: 5920
url: /zh/net/aspose.words/tablestyle/
---
## TableStyle class

表示表格样式。

```csharp
public class TableStyle : Style
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | 获取此样式的所有别名。如果样式没有别名，则返回空字符串数组。 |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | 指定表格样式的对齐方式。 |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | 获取或设置一个标志，指示是否允许表格行中的文本跨分页符进行拆分。 |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | 获取/设置此样式所基于的样式的名称。 |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | 获取或设置这是否是从右到左表格的样式。 |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | 获取样式的默认单元格边框集合。 |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | 获取或设置要添加到表格单元格内容下方的空间量（以磅为单位）。 |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | 如果此样式是 MS Word 中的内置样式之一，则为真。 |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | 获取或设置单元格之间的空间量（以磅为单位）。 |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | 获取或设置当样式指定奇数/偶数列带时要包含在带中的列数。 |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | 可能为此表格样式定义的条件样式集合。 |
| [Document](../../aspose.words/style/document/) { get; } | 获取所有者文档。 |
| [Font](../../aspose.words/style/font/) { get; } | 获取样式的字符格式。 |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | 当样式是内置标题样式之一时为真。 |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | 指定此样式是否显示在 MS Word UI 内的快速样式库中。 |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | 获取或设置表示表格左缩进的值。 |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | 获取或设置要添加到表格单元格内容左侧的空间量（以磅为单位）。 |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | 获取与该样式链接的样式的名称。如果没有链接样式，则返回空字符串。 |
| [List](../../aspose.words/style/list/) { get; } | 获取定义此列表样式格式的列表。 |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | 提供对段落样式的列表格式属性的访问。 |
| [Name](../../aspose.words/style/name/) { get; set; } | 获取或设置样式的名称。 |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | 获取/设置样式的名称，以自动应用到插入到使用指定样式格式化的 段落之后的新段落。 |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | 获取样式的段落格式。 |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | 获取或设置要添加到表格单元格内容右侧的空间量（以磅为单位）。 |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | 获取或设置当样式指定奇/偶行分带时要包含在分带中的行数。 |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | 得到一个[`Shading`](../shading/)引用表格单元格的阴影格式的对象。 |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | 获取内置样式的独立于语言环境的样式标识符。 |
| [Styles](../../aspose.words/style/styles/) { get; } | 获取该样式所属的样式集合。 |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | 获取或设置要添加到表格单元格内容之上的空间量（以磅为单位）。 |
| [Type](../../aspose.words/style/type/) { get; } | 获取样式类型（段落或字符）。 |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | 指定单元格的垂直对齐方式。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(Style) | 与指定的样式进行比较。 样式 Istds 仅针对内置样式进行比较。 样式默认值不包括在比较中。 基本样式、链接样式和下一段样式进行递归比较。 |
| [Remove](../../aspose.words/style/remove/)() | 从文档中删除指定的样式。 |

### 例子

显示如何为表格创建自定义样式设置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// 设置表格的样式属性可能会影响表格本身的属性。
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### 也可以看看

* class [Style](../style/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


