---
title: Class LayoutCollector
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Layout.LayoutCollector 班级. 此类允许计算文档节点的页码
type: docs
weight: 3320
url: /zh/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

此类允许计算文档节点的页码。

要了解更多信息，请访问[转换为固定页面格式](https://docs.aspose.com/words/net/converting-to-fixed-page-format/)文档文章。

```csharp
public class LayoutCollector
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [LayoutCollector](layoutcollector/)(Document) | 初始化此类的实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | 获取或设置此收集器实例附加到的文档。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | 清除所有收集的布局数据。手动更新文档或重建布局后调用此方法。 |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(Node) | 获取节点结束的页面的从 1 开始的索引。如果节点无法映射到页面，则返回 0。 |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(Node) | 返回一个不透明的位置[`LayoutEnumerator`](../layoutenumerator/)对应于指定的节点。 您可以使用返回值作为参数[`Current`](../layoutenumerator/current/)给定枚举的文档being 和节点的文档是相同的. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(Node) | 获取指定节点跨越的页数。如果节点位于单个页面内，则为 0。 这与[`GetEndPageIndex`](./getendpageindex/)-[`GetStartPageIndex`](./getstartpageindex/). |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(Node) | 获取节点开始的页面的从 1 开始的索引。如果节点无法映射到页面，则返回 0。 |

### 评论

当您创建一个`LayoutCollector`并指定一个[`Document`](../../aspose.words/document/)要附加到的文档对象， 当文档格式化为页面时，收集器将记录文档节点到布局对象的映射。

您将能够使用以下命令找出特定文档节点（例如，运行、段落或表格单元格）位于 的页面：[`GetStartPageIndex`](./getstartpageindex/),[`GetEndPageIndex`](./getendpageindex/)和[`GetNumPagesSpanned`](./getnumpagesspanned/)方法。 这些方法自动构建文档的页面布局模型并根据需要更新字段。

当不再需要收集布局信息时，最好设置[`Document`](./document/)财产给`无效的` 以避免不必要地收集更多布局映射。

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

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)


