---
title: LayoutCollector.Document
second_title: Aspose.Words for .NET API 参考
description: LayoutCollector 财产. 获取或设置此收集器实例附加到的文档
type: docs
weight: 20
url: /zh/net/aspose.words.layout/layoutcollector/document/
---
## LayoutCollector.Document property

获取或设置此收集器实例附加到的文档。

```csharp
public Document Document { get; set; }
```

### 评论

如果需要访问文档节点的页面索引，则需要在构建文档的页面布局之前设置此属性以指向文档实例 。最好将此属性设置为`无效的`之后， 否则收集器将继续从文档页面布局的后续重建中积累信息。

### 例子

演示如何查看节点跨越的页面范围。

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// 调用“GetNumPagesSpanned”方法来计算文档内容跨越了多少页。
// 由于文档为空，因此页数当前为零。
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

// 在布局收集器之前，我们需要调用“UpdatePageLayout”方法来给我们
// 任何与布局相关的指标的准确数字，例如页数。
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// 我们可以看到任意节点的起始页和结束页的数量以及它们的总页跨度。
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// 我们可以使用 LayoutEnumerator 迭代布局实体。
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator 可以像树一样遍历布局实体的集合。
// 我们还可以将其应用于任何节点对应的布局实体。
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [LayoutCollector](../)
* 命名空间 [Aspose.Words.Layout](../../layoutcollector/)
* 部件 [Aspose.Words](../../../)


