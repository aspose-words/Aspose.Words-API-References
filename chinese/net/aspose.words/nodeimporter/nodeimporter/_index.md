---
title: NodeImporter
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: 用于 .NET 的 Aspose.Words
description: NodeImporter 构造函数. 初始化一个新实例NodeImporter类 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/)*) {#constructor}

初始化一个新实例[`NodeImporter`](../)类.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | DocumentBase | 源文档。 |
| dstDoc | DocumentBase | 将成为导入节点所有者的目标文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并冲突的样式格式。 |

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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#constructor_1}

初始化一个新实例[`NodeImporter`](../)类.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | DocumentBase | 源文档。 |
| dstDoc | DocumentBase | 将成为导入节点所有者的目标文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并冲突的样式格式。 |
| importFormatOptions | ImportFormatOptions | 指定格式化导入节点的各种选项。 |

## 例子

显示导入具有相同列表定义标识符的列表的文档时如何解决冲突。

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// 将“KeepSourceNumbering”属性设置为“true”以应用不同的列表定义 ID
// 与 Aspose.Words 将它们导入到目标文档中的样式相同。
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

演示如何解决源文档和目标文档中的列表编号冲突。

```csharp
// 使用自定义列表编号方案打开文档，然后克隆它。
// 由于两者具有相同的编号格式，如果我们将一个文档导入到另一个文档中，格式会发生冲突。
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// 当我们将文档的克隆导入到原始文档中然后追加它时，
// 然后具有相同列表格式的两个列表将连接。
// 如果我们将“KeepSourceNumbering”标志设置为“false”，则列表会从文档克隆
// 我们附加到原始列表中的内容将继续我们附加到的列表的编号。
// 这将有效地将两个列表合并为一个。
// 如果我们将“KeepSourceNumbering”标志设置为“true”，则文档克隆
// list 将保留其原始编号，使两个列表显示为单独的列表。
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### 也可以看看

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
