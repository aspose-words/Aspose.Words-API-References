---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: 用于 .NET 的 Aspose.Words
description: Document ExpandTableStylesToDirectFormatting 方法. 将表格样式中指定的格式转换为文档中表格的直接格式 在 C#.
type: docs
weight: 590
url: /zh/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

将表格样式中指定的格式转换为文档中表格的直接格式。

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## 评论

存在此方法是因为此版本的 Aspose.Words 仅对 表格样式提供有限支持（见下文）。当您加载包含使用表格样式格式化的表格的 DOCX 或 WordprocessingML 文档并且您需要查询 表格、单元格、段落或文本的格式时，此方法可能很有用。

这个版本的 Aspose.Words 对表格样式提供了有限的支持，如下所示：

* 在将文档另存为 DOCX 或 WordprocessingML 时，DOCX 或 WordprocessingML 文档中定义的表格样式将保留为表格 styles 。
* 在将文档保存为任何其他格式、 渲染或打印时，DOCX 或 WordprocessingML 文档中定义的表格样式会自动转换为 以直接格式化表格。
* 在 DOC 文档中定义的表格样式在 仅将文档保存为 DOC 时保留为表格样式。

## 例子

演示如何将表格样式的属性直接应用于表格元素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// 此方法涉及表格样式属性，例如我们上面设置的那些。
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
