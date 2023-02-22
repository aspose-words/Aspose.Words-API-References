---
title: LayoutCollector.GetEntity
second_title: Aspose.Words for .NET API 参考
description: LayoutCollector 方法. 返回一个不透明的位置LayoutEnumerator对应于指定的节点 您可以使用返回值作为参数Current给定正在 枚举的文档和节点的文档相同.
type: docs
weight: 50
url: /zh/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

返回一个不透明的位置[`LayoutEnumerator`](../../layoutenumerator/)对应于指定的节点。 您可以使用返回值作为参数[`Current`](../../layoutenumerator/current/)给定正在 枚举的文档和节点的文档相同.

```csharp
public object GetEntity(Node node)
```

### 评论

此方法仅适用于[`Paragraph`](../../../aspose.words/paragraph/)节点，以及不可分割的内联节点， 例如[`BookmarkStart`](../../../aspose.words/bookmarkstart/)或者[`Shape`](../../../aspose.words.drawing/shape/).它不适用于[`Run`](../../../aspose.words/run/),[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/)或者[`Table`](../../../aspose.words.tables/table/)节点，以及页眉/页脚中的节点。

请注意，为 a 返回的实体[`Paragraph`](../../../aspose.words/paragraph/)节点是一个分段跨度。使用适当的方法提升到父行

如果您需要导航到[`Run`](../../../aspose.words/run/)文本然后您可以在 it 之前插入书签，然后导航到书签。

如果您需要导航到[`Cell`](../../../aspose.words.tables/cell/)节点然后你可以移动到一个[`Paragraph`](../../../aspose.words/paragraph/) 节点在此单元格中，然后上升到父实体。相同的方法可用于[`Row`](../../../aspose.words.tables/row/) 和[`Table`](../../../aspose.words.tables/table/)节点。

### 例子

显示如何查看节点跨越的页面范围。

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// 调用“GetNumPagesSpanned”方法来统计我们的文档内容跨越了多少页。
// 由于文档为空，因此当前页数为零。
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// 用 5 页内容填充文档。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// 在布局收集器之前，我们需要调用“UpdatePageLayout”方法给我们
// 任何与布局相关的指标的准确数字，例如页数。
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// 我们可以看到任何节点的起始页和结束页的数量以及它们的总页跨度。
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// 我们可以使用 LayoutEnumerator 遍历布局实体。
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator 可以像树一样遍历布局实体的集合。
// 我们也可以将它应用到任何节点对应的布局实体上。
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### 也可以看看

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* 命名空间 [Aspose.Words.Layout](../../layoutcollector/)
* 部件 [Aspose.Words](../../../)


