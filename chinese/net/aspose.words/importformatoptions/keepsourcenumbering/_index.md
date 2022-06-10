---
title: KeepSourceNumbering
second_title: Aspose.Words for .NET API 参考
description: 获取或设置一个布尔值该值指定编号在源文档和 目标文档中发生冲突时如何导入 默认值为 false 
type: docs
weight: 50
url: /zh/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

获取或设置一个布尔值，该值指定编号在源文档和 目标文档中发生冲突时如何导入。 默认值为` false` 。

```csharp
public bool KeepSourceNumbering { get; set; }
```

### 例子

显示在导入具有相同列表定义标识符的列表的文档时如何解决冲突。

```csharp
 // 打开一个带有自定义列表编号方案的文档，然后克隆它。
 // 由于两者具有相同的编号格式，如果我们将一个文档导入另一个文档，格式将发生冲突。
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

 // 当我们将文档的克隆导入到原始文件中然后附加它时，
// 那么两个列表格式相同的列表就会加入.
 // 如果我们将“KeepSourceNumbering”标志设置为“false”，那么来自文档的列表 clone
 // 我们附加到原始的将继续我们附加到的列表的编号。
 // 这将有效地将两个列表合并为一个。
 // 如果我们将“KeepSourceNumbering”标志设置为“true”，那么文档 clone
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

显示如何导入带有编号列表的文档。

```csharp
 // 打开一个带有自定义列表编号方案的文档，然后克隆它。
 // 由于两者具有相同的编号格式，如果我们将一个文档导入另一个文档，格式将发生冲突。
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

 // 当我们将文档的克隆导入到原始文件中然后附加它时，
// 那么两个列表格式相同的列表就会加入.
 // 如果我们将“KeepSourceNumbering”标志设置为“false”，那么来自文档的列表 clone
 // 我们附加到原始的将继续我们附加到的列表的编号。
 // 这将有效地将两个列表合并为一个。
 // 如果我们将“KeepSourceNumbering”标志设置为“true”，那么文档 clone
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

显示如何解决源文档和目标文档中的列表编号冲突。

```csharp
 // 打开一个带有自定义列表编号方案的文档，然后克隆它。
 // 由于两者具有相同的编号格式，如果我们将一个文档导入另一个文档，格式将发生冲突。
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

 // 当我们将文档的克隆导入到原始文件中然后附加它时，
// 那么两个列表格式相同的列表就会加入.
 // 如果我们将“KeepSourceNumbering”标志设置为“false”，那么来自文档的列表 clone
 // 我们附加到原始的将继续我们附加到的列表的编号。
 // 这将有效地将两个列表合并为一个。
 // 如果我们将“KeepSourceNumbering”标志设置为“true”，那么文档 clone
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

* class [ImportFormatOptions](../../importformatoptions)
* 命名空间 [Aspose.Words](../../importformatoptions)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
