---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.NodeImporter 轻松传输文档节点。立即简化您的工作流程并提升文档管理效率！
type: docs
weight: 4900
url: /zh/net/aspose.words/nodeimporter/
---
## NodeImporter class

允许高效地执行从一个文档到另一个文档的节点重复导入。

要了解更多信息，请访问[Aspose.Words 文档对象模型（DOM）](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class NodeImporter
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | 初始化`NodeImporter`类. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | 初始化`NodeImporter`类. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | 将节点从一个文档导入到另一个文档。 |

## 评论

Aspose.Words 提供了在 Microsoft Word 文档之间轻松复制和移动片段的功能。这被称为“导入节点”。在将片段从一个文档插入另一个文档之前，您需要先“导入”它。导入操作会创建原始节点的深度克隆，以便将其插入到目标文档中。

导入节点的最简单方法是使用[`ImportNode`](../documentbase/importnode/)method 提供[`DocumentBase`](../documentbase/)目的。

但是，当您需要多次将节点从一个文档导入另一个文档时， 最好使用`NodeImporter`类。`NodeImporter` 类允许最小化目标文档中创建的样式和列表的数量。

将片段从一个 Microsoft Word 文档复制或移动到另一个文档，对 Aspose.Words 来说，带来了诸多技术挑战。在 Word 文档中，样式和列表格式是集中存储的，与文档文本分开存储。段落和文本片段仅通过内部唯一标识符引用样式。

挑战源于不同文档中的样式和列表不同。例如，要将采用标题 1 样式格式化的段落从一个文档复制到另一个文档，必须考虑许多事项：决定是否将标题 1 样式从源文档复制到目标文档，克隆该段落，更新克隆的段落，以便它引用目标文档中正确的标题 1 样式。如果必须复制样式，则应分析它引用的所有样式（基于样式和下一个段落样式），并可能复制它们，等等。复制项目符号或编号段落时也存在类似的问题，因为 Microsoft Word 将列表定义与文本分开存储。

这`NodeImporter`类类似于上下文，用于在导入期间保存“翻译表”。它可以在源文档和目标文档中的样式和列表之间进行正确的转换。

## 例子

展示如何将一个文档的内容插入到另一个文档的书签中。

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
/// 将文档内容插入到指定节点后。
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // 循环遍历节主体中的所有块级节点，
        // 然后克隆并插入不是部分最后一个空段落的每个节点。
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
