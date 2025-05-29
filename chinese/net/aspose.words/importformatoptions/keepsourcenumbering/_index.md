---
title: ImportFormatOptions.KeepSourceNumbering
linktitle: KeepSourceNumbering
articleTitle: KeepSourceNumbering
second_title: Aspose.Words for .NET
description: 使用 ImportFormatOptions KeepSourceNumbering 属性控制文档编号。轻松管理冲突，实现无缝导入。默认值为 false。
type: docs
weight: 60
url: /zh/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

获取或设置一个布尔值，该值指定当源文档和目标文档中的编号发生冲突时如何导入编号。 默认值为`错误的`.

```csharp
public bool KeepSourceNumbering { get; set; }
```

## 例子

展示如何在导入包含相同列表定义标识符的列表的文档时解决冲突。

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// 将“KeepSourceNumbering”属性设置为“true”以应用不同的列表定义 ID
// 与 Aspose.Words 导入到目标文档中的样式相同。
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

展示如何导入带有编号列表的文档。

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// 如果列表样式发生冲突，则应用源文档的列表格式。
// 将“KeepSourceNumbering”属性设置为“false”以不将任何列表编号导入目标文档。
// 将“KeepSourceNumbering”属性设置为“true”导入所有冲突
// 列出与源文档中相同的样式编号。
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

展示如何解决源文档和目标文档中的列表编号冲突。

```csharp
// 打开具有自定义列表编号方案的文档，然后克隆它。
// 由于两者具有相同的编号格式，如果我们将一个文档导入另一个文档，格式就会发生冲突。
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// 当我们将文档的克隆导入到原始文档中，然后将其附加到原始文档中时，
// 那么具有相同列表格式的两个列表将会合并。
// 如果我们将“KeepSourceNumbering”标志设置为“false”，则文档中的列表将克隆
// 我们附加到原始内容后的内容将延续我们将其附加到的列表的编号。
// 这将有效地将两个列表合并为一个。
// 如果我们将“KeepSourceNumbering”标志设置为“true”，则文档克隆
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

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
