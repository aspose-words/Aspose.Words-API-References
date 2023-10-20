---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.NodeImporter 班级. 允许高效地将节点从一个文档重复导入到另一个文档 在 C#.
type: docs
weight: 4210
url: /zh/net/aspose.words/nodeimporter/
---
## NodeImporter class

允许高效地将节点从一个文档重复导入到另一个文档。

要了解更多信息，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class NodeImporter
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | 初始化一个新实例`NodeImporter`类. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | 初始化一个新实例`NodeImporter`类. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | 将一个节点从一个文档导入到另一个文档中。 |

## 评论

Aspose.Words 提供了在 Microsoft Word 文档之间轻松复制和移动fragments 的功能。这称为“导入节点”。 在将一个文档的片段插入另一个文档之前，您需要“导入”它。 导入会创建原始节点的深度克隆，准备插入到 目标文档中。

导入节点最简单的方法是使用[`ImportNode`](../documentbase/importnode/)method 由提供[`DocumentBase`](../documentbase/)目的。

但是，当您需要多次将节点从一个文档导入到另一个文档时， 最好使用`NodeImporter`班级。这`NodeImporter` 类允许最大限度地减少目标文档中创建的样式和列表的数量。

将片段从一个 Microsoft Word 文档复制或移动到另一个文档给 Aspose.Words 带来了无数的技术挑战。在Word文档中，样式和列表格式 与文档文本分开集中存储。 paragraphs 和文本串仅通过内部唯一标识符引用样式。

挑战源于不同文档中的样式和列表不同。 例如，要将采用标题 1 样式格式化的段落从一个文档复制到另一个文档， 必须考虑许多事项：决定是否将标题 1 样式从源文档的 复制到目标文档，克隆该段落，更新克隆的 段落，使其引用目标文档中正确的标题 1 样式。 如果必须复制该样式，则它所复制的所有样式参考文献（基于 style 和下一段样式）也应该进行分析，并可能进行复制等等。 复制带项目符号或编号的段落时存在类似问题，因为 Microsoft Word 将列表定义与文本分开存储。

这`NodeImporter`类就像一个上下文，在导入期间保存“翻译表” 。它可以正确地在源文档和 目标文档中的样式和列表之间进行转换。

## 例子

演示如何将一个文档的内容插入到另一文档的书签中。

```csharp
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// 在指定节点之后插入文档的内容。
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // 循环节体中的所有块级节点，
        // 然后克隆并插入不是节的最后一个空段落的每个节点。
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
