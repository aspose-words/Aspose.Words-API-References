---
title: NodeImporter
second_title: Справочник по API Aspose.Words для .NET
description: Инициализирует новый экземплярNodeImporteraspose.words/nodeimporter класс.
type: docs
weight: 10
url: /ru/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

Инициализирует новый экземпляр[`NodeImporter`](../../nodeimporter) класс.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | DocumentBase | Исходный документ. |
| dstDoc | DocumentBase | Целевой документ, который будет владельцем импортированных узлов. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующее форматирование стилей. |

### Примеры

Показывает, как вставить содержимое одного документа в закладку в другом документе.

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
/// Вставляет содержимое документа после указанного узла.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Перебрать все узлы блочного уровня в теле раздела,
        // затем клонируем и вставляем каждый узел, который не является последним пустым абзацем раздела.
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

### Смотрите также

* class [DocumentBase](../../documentbase)
* enum [ImportFormatMode](../../importformatmode)
* class [NodeImporter](../../nodeimporter)
* пространство имен [Aspose.Words](../../nodeimporter)
* сборка [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

Инициализирует новый экземпляр[`NodeImporter`](../../nodeimporter) класс.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | DocumentBase | Исходный документ. |
| dstDoc | DocumentBase | Целевой документ, который будет владельцем импортированных узлов. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующее форматирование стилей. |
| importFormatOptions | ImportFormatOptions | Задает различные параметры форматирования импортированного узла. |

### Примеры

Показывает, как разрешить конфликт при импорте документов, содержащих списки с одинаковым идентификатором определения списка.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Установите для свойства "KeepSourceNumbering" значение "true", чтобы применить другой идентификатор определения списка
// в идентичные стили, поскольку Aspose.Words импортирует их в целевые документы.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Показывает, как разрешать конфликты нумерации списков в исходном и целевом документах.

```csharp
// Откройте документ с пользовательской схемой нумерации списков, а затем клонируйте его.
// Так как оба имеют одинаковый формат нумерации, форматы будут конфликтовать, если мы импортируем один документ в другой.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Когда мы импортируем клон документа в оригинал, а затем добавляем его,
// тогда объединятся два списка с одинаковым форматом списка.
// Если установить флаг "KeepSourceNumbering" в "false", то список из клона документа
// который мы добавляем к оригиналу, будет продолжать нумерацию списка, к которому мы его добавляем.
// Это эффективно объединит два списка в один.
// Если мы установим флаг "KeepSourceNumbering" в "true", то клон документа
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

* class [DocumentBase](../../documentbase)
* enum [ImportFormatMode](../../importformatmode)
* class [ImportFormatOptions](../../importformatoptions)
* class [NodeImporter](../../nodeimporter)
* пространство имен [Aspose.Words](../../nodeimporter)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
