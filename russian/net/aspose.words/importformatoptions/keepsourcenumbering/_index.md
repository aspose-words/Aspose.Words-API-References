---
title: ImportFormatOptions.KeepSourceNumbering
linktitle: KeepSourceNumbering
articleTitle: KeepSourceNumbering
second_title: Aspose.Words для .NET
description: Управляйте нумерацией документов с помощью свойства ImportFormatOptions KeepSourceNumbering. Легко управляйте конфликтами для бесшовного импорта. По умолчанию — false.
type: docs
weight: 60
url: /ru/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Возвращает или задает логическое значение, указывающее, как будет импортироваться нумерация при ее конфликте в исходном и целевом документах. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

## Примеры

Показывает, как устранить конфликт при импорте документов, содержащих списки с одинаковым идентификатором определения списка.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Установите свойство «KeepSourceNumbering» в значение «true», чтобы применить другой идентификатор определения списка
// к тем же стилям, которые Aspose.Words импортирует в целевые документы.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Показывает, как импортировать документ с нумерованными списками.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// Если есть конфликт стилей списка, применяем формат списка исходного документа.
// Установите свойство «KeepSourceNumbering» в значение «false», чтобы не импортировать какие-либо номера списков в целевой документ.
// Установите свойство "KeepSourceNumbering" в значение "true", импортируйте все конфликтующие
// нумерация в стиле списка с тем же внешним видом, что и в исходном документе.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Показывает, как разрешать конфликты нумерации списков в исходных и целевых документах.

```csharp
// Откройте документ с пользовательской схемой нумерации списков, а затем клонируйте его.
// Поскольку оба документа имеют одинаковый формат нумерации, форматы будут конфликтовать, если мы импортируем один документ в другой.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Когда мы импортируем клон документа в оригинал, а затем добавляем его,
// тогда два списка с одинаковым форматом списка будут объединены.
// Если мы установим флаг "KeepSourceNumbering" в значение "false", то список из клона документа
// который мы добавляем к оригиналу, будет продолжать нумерацию списка, к которому мы его добавляем.
// Это фактически объединит два списка в один.
// Если мы установим флаг "KeepSourceNumbering" в значение "true", то клон документа
 // список сохранит свою первоначальную нумерацию, благодаря чему два списка будут отображаться как отдельные списки.
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

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
