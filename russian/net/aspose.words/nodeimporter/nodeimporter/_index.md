---
title: NodeImporter
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор NodeImporter, с легкостью создавайте новые экземпляры NodeImporter, чтобы оптимизировать управление данными и повысить эффективность проекта.
type: docs
weight: 10
url: /ru/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/)*) {#constructor}

Инициализирует новый экземпляр[`NodeImporter`](../) класс.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | DocumentBase | Исходный документ. |
| dstDoc | DocumentBase | Целевой документ, который будет владельцем импортированных узлов. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующие стили форматирования. |

## Примеры

Показывает, как вставить содержимое одного документа в закладку другого документа.

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
/// Вставляет содержимое документа после указанного узла.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Проходим по всем узлам уровня блока в теле раздела,
        // затем клонировать и вставить каждый узел, который не является последним пустым абзацем раздела.
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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#constructor_1}

Инициализирует новый экземпляр[`NodeImporter`](../) класс.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | DocumentBase | Исходный документ. |
| dstDoc | DocumentBase | Целевой документ, который будет владельцем импортированных узлов. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующие стили форматирования. |
| importFormatOptions | ImportFormatOptions | Задает различные параметры форматирования импортированного узла. |

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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
