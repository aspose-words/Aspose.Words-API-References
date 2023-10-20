---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Tables.Table 班级. 表示 Word 文档中的表格 在 C#.
type: docs
weight: 6340
url: /zh/net/aspose.words.tables/table/
---
## Table class

表示 Word 文档中的表格。

要了解更多信息，请访问[使用表格](https://docs.aspose.com/words/net/working-with-tables/)文档文章。

```csharp
public class Table : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | 初始化一个新实例`Table`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | 获取或设置由表属性指定的绝对水平浮动表位置，以点为单位。 默认值为 0。 |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | 获取或设置由表属性指定的绝对垂直浮动表位置，以点为单位。 默认值为 0。 |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | 指定内联表在文档中的对齐方式。 |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | 允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适合其内容。 |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | 获取或设置“允许单元格之间的间距”选项。 |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | 获取浮动表是否允许文档中的其他浮动对象 在显示时重叠其范围。 默认值为`真的`. |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | 获取或设置这是否是从右到左的表格。 |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | 获取或设置要在单元格内容下方添加的空间量（以磅为单位）。 |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | 获取或设置单元格之间的空间量（以磅为单位）。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | 获取或设置此表的描述。 它提供表中包含的信息的替代文本表示形式。 |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | 获取或设置表格底部与周围文本之间的距离（以磅为单位）。 |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | 获取或设置表格左侧与周围文本之间的距离（以磅为单位）。 |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | 获取或设置表格右侧与周围文本之间的距离（以磅为单位）。 |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | 获取或设置桌面与周围文本之间的距离（以磅为单位）。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | 返回第一个[`Row`](../row/)表中的节点. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果该节点有任何子节点. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | 获取计算浮动台水平位置的基础对象。 默认值为Column. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为该节点可以有子节点。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | 返回最后一个[`Row`](../row/)表中的节点. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | 获取或设置表示表格左缩进的值。 |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | 获取或设置要添加到单元格内容左侧的空间量（以磅为单位）。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | 返回Table. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | 获取或设置表格首选宽度。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | 获取或设置浮动表相对水平对齐方式。 |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | 获取或设置浮动表相对垂直对齐方式。 |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | 获取或设置要添加到单元格内容右侧的空间量（以磅为单位）。 |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | 提供对表行的类型化访问。 |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | 获取或设置应用于此表的表格样式。 |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | 获取或设置应用于此表的表样式的区域设置独立样式标识符。 |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | 获取或设置应用于此表的表格样式的名称。 |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | 获取或设置指定如何将表样式应用于此表的位标志。 |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | 获取或设置[`TextWrapping`](./textwrapping/)对于表. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | 获取或设置此表的标题。 它提供表中包含的信息的替代文本表示形式。 |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | 获取或设置要在单元格内容上方添加的空间量（以磅为单位）。 |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | 获取计算浮动台垂直位置的基础对象。 默认值为Margin. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | 根据指定的自动调整行为调整表格和单元格的大小。 |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | 删除此表上的所有表格和单元格边框。 |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | 删除桌子上的所有阴影。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | 将按宽度水平合并的单元格转换为按[`HorizontalMerge`](../cellformat/horizontalmerge/). |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | 如果表没有行，则创建并追加一行[`Row`](../row/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | 在指定的引用节点之后立即插入指定的节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | 在指定的引用节点之前插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据先序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | 删除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../../aspose.words/node/)与 XPath 表达式匹配。 |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | 将指定的表格边框设置为指定的线条样式、宽度和颜色。 |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | 将所有表格边框设置为指定的线条样式、宽度和颜色。 |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | 将整个表的底纹设置为指定值。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点的内容导出到字符串中。 |

## 评论

`Table`是一个块级节点，可以是派生类的子节点[`Story`](../../aspose.words/story/)或 [`InlineStory`](../../aspose.words/inlinestory/)。

`Table`可以包含一个或多个[`Row`](../row/)节点。

最小有效表需要至少有一个[`Row`](../row/)。

## 例子

展示如何创建表。

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// 表格包含行，行包含单元格，单元格可能包含段落
// 具有典型元素，例如运行、形状，甚至其他表格。
// 在表上调用“EnsureMinimum”方法将确保
// 该表格至少有一行、一个单元格和一个段落。
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// 将文本添加到表第一行中的第一个调用。
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

演示如何迭代文档中的所有表格并打印每个单元格的内容。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // 我们可以对行集合使用“ToArray”方法将其克隆到数组中。
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // 我们可以对单元集合使用“ToArray”方法将其克隆到数组中。
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

演示如何构建格式化的 2x2 表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// 构建表时，文档构建器将应用其当前的 RowFormat/CellFormat 属性值
// 到其光标所在的当前行/单元格以及创建它们时的任何新行/单元格。
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// 先前添加的行和单元格不会受到构建器格式更改的影响。
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

演示如何在不使用文档生成器的情况下构建嵌套表。

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // 创建三行四列的外表，然后将其添加到文档中。
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // 创建另一个包含两行和两列的表格，然后将其插入到第一个表格的第一个单元格中。
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// 在文档中创建一个新表格，每个单元格中具有给定的尺寸和文本。
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // 您可以使用“标题”和“描述”属性分别向表格添加标题和描述。
    // 在我们可以使用这些属性之前，表必须至少有一行。
    // 这些属性对于符合 ISO / IEC 29500 的 .docx 文档有意义（请参阅 OoxmlCompliance 类）。
    // 如果我们将文档保存为 ISO/IEC 29500 之前的格式，Microsoft Word 将忽略这些属性。
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### 也可以看看

* class [CompositeNode](../../aspose.words/compositenode/)
* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)
