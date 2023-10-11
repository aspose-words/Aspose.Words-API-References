---
title: NodeImporter.ImportNode
second_title: Aspose.Words for .NET API 参考
description: NodeImporter 方法. 将一个节点从一个文档导入到另一个文档中
type: docs
weight: 20
url: /zh/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

将一个节点从一个文档导入到另一个文档中。

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | Node | 要导入的节点。 |
| isImportChildren | Boolean | `真的`递归导入所有子节点；否则，`错误的`。 |

### 返回值

克隆的导入节点。该节点属于目标文档，但没有父节点。

### 评论

导入节点会创建属于导入文档的源节点的副本。 返回的节点没有父节点。源节点不会从原始文档中更改或删除。

在将另一个文档中的节点插入到此文档中之前，必须将其导入。 在导入期间，特定于文档的属性（例如对样式和列表的引用）将从原始文档翻译 到导入文档。导入节点后，可以使用将其插入 到文档中的适当位置Node)或 Node)。

如果源节点已经属于目标文档，则只需创建源节点的深层clone 。

### 例子

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

* class [Node](../../node/)
* class [NodeImporter](../)
* 命名空间 [Aspose.Words](../../nodeimporter/)
* 部件 [Aspose.Words](../../../)


