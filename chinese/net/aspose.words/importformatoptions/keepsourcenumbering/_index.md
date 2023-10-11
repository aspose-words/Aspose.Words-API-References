---
title: ImportFormatOptions.KeepSourceNumbering
second_title: Aspose.Words for .NET API 参考
description: ImportFormatOptions 财产. 获取或设置一个布尔值该值指定当编号与源文档和 目标文档发生冲突时如何导入编号 默认值为错误的.
type: docs
weight: 60
url: /zh/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

获取或设置一个布尔值，该值指定当编号与源文档和 目标文档发生冲突时如何导入编号。 默认值为`错误的`.

```csharp
public bool KeepSourceNumbering { get; set; }
```

### 例子

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

演示如何导入带有编号列表的文档。

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// 如果列表样式冲突，则应用源文档的列表格式。
// 将“KeepSourceNumbering”属性设置为“false”，以不将任何列表编号导入到目标文档中。
// 将“KeepSourceNumbering”属性设置为“true”导入所有冲突
// 列表样式编号的外观与源文档中的外观相同。
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
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

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../importformatoptions/)
* 部件 [Aspose.Words](../../../)


