---
title: Paragraph.IsEndOfSection
linktitle: IsEndOfSection
articleTitle: IsEndOfSection
second_title: 用于 .NET 的 Aspose.Words
description: Paragraph IsEndOfSection 财产. 如果该段落是最后一段则为 TrueBody 正文故事aSection否则为假 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words/paragraph/isendofsection/
---
## Paragraph.IsEndOfSection property

如果该段落是最后一段，则为 True[`Body`](../../body/) （正文故事）a[`Section`](../../section/);否则为假。

```csharp
public bool IsEndOfSection { get; }
```

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

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
