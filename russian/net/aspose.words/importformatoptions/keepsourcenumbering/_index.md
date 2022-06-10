---
title: KeepSourceNumbering
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает логическое значение указывающее как будет импортироваться нумерация если она конфликтует в исходном и целевом документах. Значение по умолчанию false .
type: docs
weight: 50
url: /ru/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Получает или задает логическое значение, указывающее, как будет импортироваться нумерация, если она конфликтует в исходном и целевом документах. Значение по умолчанию:` false` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

### Примеры

Показывает, как разрешить конфликт при импорте документов, содержащих списки с одинаковым идентификатором определения списка.

```csharp
 // Открыть документ с пользовательской схемой нумерации списков, а затем клонировать его.
 // Поскольку оба имеют одинаковый формат нумерации, форматы будут конфликтовать, если мы импортируем один документ в другой.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

 // Когда мы импортируем клон документа в оригинал, а затем добавляем его, 
// тогда объединятся два списка с одинаковым форматом списка.
 // Если установить флаг "KeepSourceNumbering" в "false", то список из документа clone
 // который мы добавляем к оригиналу, будет продолжать нумерацию списка, к которому мы его добавляем.
 // Это эффективно объединит два списка в один.
 // Если мы установим флаг "KeepSourceNumbering" в "true", то документ clone
 // список сохранит исходную нумерацию, благодаря чему два списка будут отображаться как отдельные списки. 
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

Показывает, как импортировать документ с нумерованными списками.

```csharp
 // Открыть документ с пользовательской схемой нумерации списков, а затем клонировать его.
 // Поскольку оба имеют одинаковый формат нумерации, форматы будут конфликтовать, если мы импортируем один документ в другой.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

 // Когда мы импортируем клон документа в оригинал, а затем добавляем его, 
// тогда объединятся два списка с одинаковым форматом списка.
 // Если установить флаг "KeepSourceNumbering" в "false", то список из документа clone
 // который мы добавляем к оригиналу, будет продолжать нумерацию списка, к которому мы его добавляем.
 // Это эффективно объединит два списка в один.
 // Если мы установим флаг "KeepSourceNumbering" в "true", то документ clone
 // список сохранит исходную нумерацию, благодаря чему два списка будут отображаться как отдельные списки. 
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

Показывает, как разрешать конфликты нумерации списков в исходном и целевом документах.

```csharp
 // Открыть документ с пользовательской схемой нумерации списков, а затем клонировать его.
 // Поскольку оба имеют одинаковый формат нумерации, форматы будут конфликтовать, если мы импортируем один документ в другой.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

 // Когда мы импортируем клон документа в оригинал, а затем добавляем его, 
// тогда объединятся два списка с одинаковым форматом списка.
 // Если установить флаг "KeepSourceNumbering" в "false", то список из документа clone
 // который мы добавляем к оригиналу, будет продолжать нумерацию списка, к которому мы его добавляем.
 // Это эффективно объединит два списка в один.
 // Если мы установим флаг "KeepSourceNumbering" в "true", то документ clone
 // список сохранит исходную нумерацию, благодаря чему два списка будут отображаться как отдельные списки. 
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

### Смотрите также

* class [ImportFormatOptions](../../importformatoptions)
* namespace [Aspose.Words](../../importformatoptions)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
