---
title: NodeImporter.NodeImporter
second_title: Aspose.Words for .NET API 参考
description: NodeImporter 构造函数. 初始化NodeImporter类.
type: docs
weight: 10
url: /zh/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

初始化[`NodeImporter`](../)类.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | DocumentBase | 源文档。 |
| dstDoc | DocumentBase | 将成为导入节点所有者的目标文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并有冲突的样式格式。 |

### 例子

演示如何将一个文档的内容插入到另一个文档的书签中。

```csharp
[Test]
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

        // 循环遍历部分主体中的所有块级节点，
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
* 命名空间 [Aspose.Words](../../nodeimporter/)
* 部件 [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

初始化[`NodeImporter`](../)类.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | DocumentBase | 源文档。 |
| dstDoc | DocumentBase | 将成为导入节点所有者的目标文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并有冲突的样式格式。 |
| importFormatOptions | ImportFormatOptions | 指定格式化导入节点的各种选项。 |

### 例子

显示在导入具有相同列表定义标识符的列表的文档时如何解决冲突。

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// 将“KeepSourceNumbering”属性设置为“true”以应用不同的列表定义 ID
// 以与 Aspose.Words 相同的样式将它们导入目标文档。
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

显示如何解决源文档和目标文档中的列表编号冲突。

```csharp
// 打开具有自定义列表编号方案的文档，然后克隆它。
// 由于两者具有相同的编号格式，如果我们将一个文档导入另一个文档，格式将发生冲突。
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// 当我们将文档的克隆导入到原始文件中然后附加它时，
// 那么两个具有相同列表格式的列表将加入。
// 如果我们将“KeepSourceNumbering”标志设置为“false”，则从文档中克隆列表
// 我们附加到原始的将继续我们附加到的列表的编号。
// 这将有效地将两个列表合并为一个。
// 如果我们将“KeepSourceNumbering”标志设置为“true”，那么文档克隆
// 列表将保留其原始编号，使两个列表显示为单独的列表。 
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
* 命名空间 [Aspose.Words](../../nodeimporter/)
* 部件 [Aspose.Words](../../../)


