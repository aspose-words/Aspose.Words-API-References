---
title: Cell
second_title: Aspose.Words for .NET API 参考
description: 表示表格单元格
type: docs
weight: 5890
url: /zh/net/aspose.words.tables/cell/
---
## Cell class

表示表格单元格。

```csharp
public class Cell : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Cell](cell)(DocumentBase) | 初始化 **Cell** 类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CellFormat](../../aspose.words.tables/cell/cellformat) { get; } | 提供对单元格格式属性的访问。 |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | 获取该节点的所有直接子节点。 |
| [Count](../../aspose.words/compositenode/count) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words.tables/cell/firstparagraph) { get; } | 获取直接子级中的第一段。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | 如果此节点有任何子节点，则返回 true。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | 返回真，因为该节点可以有子节点。 |
| [IsFirstCell](../../aspose.words.tables/cell/isfirstcell) { get; } | 如果这是一行中的第一个单元格，则为真；否则为假。 |
| [IsLastCell](../../aspose.words.tables/cell/islastcell) { get; } | 如果这是一行中的最后一个单元格，则为真；否则为假。 |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words.tables/cell/lastparagraph) { get; } | 获取直接子级中的最后一段。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟该节点的节点。 |
| override [NodeType](../../aspose.words.tables/cell/nodetype) { get; } | 返回 **NodeType.Cell** 。 |
| [Paragraphs](../../aspose.words.tables/cell/paragraphs) { get; } | 获取作为单元格直接子级的段落的集合。 |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [ParentRow](../../aspose.words.tables/cell/parentrow) { get; } | 返回单元格的父行。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回 **Range** 对象，该对象表示包含在此节点中的文档部分。 |
| [Tables](../../aspose.words.tables/cell/tables) { get; } | 获取作为单元格直接子级的表的集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.tables/cell/accept)(DocumentVisitor) | 接受访问者。 |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | 保留供系统使用。 IXPath 可导航。 |
| [EnsureMinimum](../../aspose.words.tables/cell/ensureminimum)() | 如果最后一个孩子不是段落，则创建并附加一个空段落。 |
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
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

**单元格** 只能成为 **行** 的孩子。

**单元格** 可以包含块级节点 **段落** 和 **表** 。

一个最小有效单元格需要至少有一个 **段落** 。

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
* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
