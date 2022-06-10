---
title: Table
second_title: Aspose.Words for .NET API 参考
description: 表示 Word 文档中的表格
type: docs
weight: 5990
url: /zh/net/aspose.words.tables/table/
---
## Table class

表示 Word 文档中的表格。

```csharp
public class Table : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Table](table)(DocumentBase) | 初始化 **表** 类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance) { get; set; } | 获取或设置表格属性指定的绝对水平浮动表格位置，以磅为单位。 默认值为 0。 |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance) { get; set; } | 获取或设置表格属性指定的绝对垂直浮动表格位置，以磅为单位。 默认值为 0。 |
| [Alignment](../../aspose.words.tables/table/alignment) { get; set; } | 指定内联表在文档中的对齐方式。 |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit) { get; set; } | 允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适应其内容。 |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing) { get; set; } | 获取或设置“允许单元格之间的间距”选项。 |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap) { get; } | 获取浮动表是否允许文档 中的其他浮动对象在显示时重叠其范围。 默认值为` true` 。 |
| [Bidi](../../aspose.words.tables/table/bidi) { get; set; } | 获取或设置这是一个从右到左的表。 |
| [BottomPadding](../../aspose.words.tables/table/bottompadding) { get; set; } | 获取或设置要添加到单元格内容下方的空间量（以磅为单位）。 |
| [CellSpacing](../../aspose.words.tables/table/cellspacing) { get; set; } | 获取或设置单元格之间的空间量（以磅为单位）。 |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | 获取该节点的所有直接子节点。 |
| [Count](../../aspose.words/compositenode/count) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| [Description](../../aspose.words.tables/table/description) { get; set; } | 获取或设置此表的描述。 它提供表中包含的信息的替代文本表示。 |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom) { get; } | 获取表格底部和周围文本之间的距离，以磅为单位。 |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft) { get; } | 获取表格左侧与周围文本之间的距离，以磅为单位。 |
| [DistanceRight](../../aspose.words.tables/table/distanceright) { get; } | 获取表格右侧与周围文本之间的距离，以磅为单位。 |
| [DistanceTop](../../aspose.words.tables/table/distancetop) { get; } | 获取桌面与周围文本之间的距离，以磅为单位。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | 获取节点的第一个子节点。 |
| [FirstRow](../../aspose.words.tables/table/firstrow) { get; } | 返回表中的第一个 **行** 节点。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | 如果此节点有任何子节点，则返回 true。 |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor) { get; set; } | 获取计算浮动表水平位置的基础对象。 默认值为Column。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | 返回真，因为该节点可以有子节点。 |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | 获取节点的最后一个子节点。 |
| [LastRow](../../aspose.words.tables/table/lastrow) { get; } | 返回表中的最后一个 **行** 节点。 |
| [LeftIndent](../../aspose.words.tables/table/leftindent) { get; set; } | 获取或设置表示表格左缩进的值。 |
| [LeftPadding](../../aspose.words.tables/table/leftpadding) { get; set; } | 获取或设置要添加到单元格内容左侧的空间量（以磅为单位）。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟该节点的节点。 |
| override [NodeType](../../aspose.words.tables/table/nodetype) { get; } | 返回 **NodeType.Table** 。 |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth) { get; set; } | 获取或设置表格首选宽度。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回 **Range** 对象，该对象表示包含在此节点中的文档部分。 |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment) { get; set; } | 获取或设置浮动表格相对水平对齐方式。 |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment) { get; set; } | 获取或设置浮动表格相对垂直对齐方式。 |
| [RightPadding](../../aspose.words.tables/table/rightpadding) { get; set; } | 获取或设置要添加到单元格内容右侧的空间量（以磅为单位）。 |
| [Rows](../../aspose.words.tables/table/rows) { get; } | 提供对表行的类型化访问。 |
| [Style](../../aspose.words.tables/table/style) { get; set; } | 获取或设置应用于此表格的表格样式。 |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier) { get; set; } | 获取或设置应用于此表的表样式的区域设置独立样式标识符。 |
| [StyleName](../../aspose.words.tables/table/stylename) { get; set; } | 获取或设置应用于此表格的表格样式的名称。 |
| [StyleOptions](../../aspose.words.tables/table/styleoptions) { get; set; } | 获取或设置指定如何将表格样式应用于此表格的位标志。 |
| [TextWrapping](../../aspose.words.tables/table/textwrapping) { get; set; } | 获取或设置[`TextWrapping`](./textwrapping)用于表。 |
| [Title](../../aspose.words.tables/table/title) { get; set; } | 获取或设置此表的标题。 它提供表中包含的信息的替代文本表示。 |
| [TopPadding](../../aspose.words.tables/table/toppadding) { get; set; } | 获取或设置要添加到单元格内容上方的空间量（以磅为单位）。 |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor) { get; set; } | 获取计算浮动表垂直定位的基础对象。 默认值为Margin。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept)(DocumentVisitor) | 接受访问者。 |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [AutoFit](../../aspose.words.tables/table/autofit)(AutoFitBehavior) | 根据指定的自动调整行为调整表格和单元格的大小。 |
| [ClearBorders](../../aspose.words.tables/table/clearborders)() | 删除该表格上的所有表格和单元格边框。 |
| [ClearShading](../../aspose.words.tables/table/clearshading)() | 移除桌子上的所有阴影。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells)() | 将按宽度水平合并的单元格转换为按[`HorizontalMerge`](../cellformat/horizontalmerge)合并的单元格。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | 保留供系统使用。 IXPath 可导航。 |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum)() | 如果表没有行，则创建并附加一个 **行** 。 |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定[`NodeType`](../../aspose.words/nodetype)的第一个祖先。 |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | 为在此节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext)() | 获取该节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | 在指定参考节点之后立即插入指定节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | 在指定参考节点之前插入指定节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove)() | 从父级中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | 移除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | 删除当前节点的所有[`SmartTag`](../../aspose.words.markup/smarttag)后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | 选择与 XPath 表达式匹配的第一个节点。 |
| [SetBorder](../../aspose.words.tables/table/setborder)(BorderType, LineStyle, double, Color, bool) | 将指定的表格边框设置为指定的线型、宽度和颜色。 |
| [SetBorders](../../aspose.words.tables/table/setborders)(LineStyle, double, Color) | 将所有表格边框设置为指定的线型、宽度和颜色。 |
| [SetShading](../../aspose.words.tables/table/setshading)(TextureIndex, Color, Color) | 为整个表的指定值设置底纹。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

**表** 是块级节点，可以是派生自 **Story** 或  **InlineStory**的类的子节点 。

**表** 可以包含一个或多个 **行** 个节点。

一个最小的有效表需要至少有一个 **Row** 。

### 例子

显示如何创建表。

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

     // 创建三行四列的外部表，然后添加到文档中。
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

     // 创建另一个两行两列的表，然后将其插入到第一个表的第一个单元格中。
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

    // 您可以使用“标题”和“描述”属性分别为您的表格添加标题和描述。
     // 表格必须至少有一行才能使用这些属性。
     // 这些属性对于符合 ISO/IEC 29500 的 .docx 文档有意义（请参阅 OoxmlCompliance 类）。
     // 如果我们将文档保存为 pre-ISO/IEC 29500 格式，Microsoft Word 会忽略这些属性。
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

显示如何遍历文档中的所有表格并打印每个单元格的内容。

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

     // 创建三行四列的外部表，然后添加到文档中。
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

     // 创建另一个两行两列的表，然后将其插入到第一个表的第一个单元格中。
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

    // 您可以使用“标题”和“描述”属性分别为您的表格添加标题和描述。
     // 表格必须至少有一行才能使用这些属性。
     // 这些属性对于符合 ISO/IEC 29500 的 .docx 文档有意义（请参阅 OoxmlCompliance 类）。
     // 如果我们将文档保存为 pre-ISO/IEC 29500 格式，Microsoft Word 会忽略这些属性。
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

显示如何构建格式化的 2x2 表。

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

     // 创建三行四列的外部表，然后添加到文档中。
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

     // 创建另一个两行两列的表，然后将其插入到第一个表的第一个单元格中。
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

    // 您可以使用“标题”和“描述”属性分别为您的表格添加标题和描述。
     // 表格必须至少有一行才能使用这些属性。
     // 这些属性对于符合 ISO/IEC 29500 的 .docx 文档有意义（请参阅 OoxmlCompliance 类）。
     // 如果我们将文档保存为 pre-ISO/IEC 29500 格式，Microsoft Word 会忽略这些属性。
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

展示如何在不使用文档构建器的情况下构建嵌套表。

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

     // 创建三行四列的外部表，然后添加到文档中。
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

     // 创建另一个两行两列的表，然后将其插入到第一个表的第一个单元格中。
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

    // 您可以使用“标题”和“描述”属性分别为您的表格添加标题和描述。
     // 表格必须至少有一行才能使用这些属性。
     // 这些属性对于符合 ISO/IEC 29500 的 .docx 文档有意义（请参阅 OoxmlCompliance 类）。
     // 如果我们将文档保存为 pre-ISO/IEC 29500 格式，Microsoft Word 会忽略这些属性。
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### 也可以看看

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Tables](../../aspose.words.tables)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
