---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words для .NET
description: Легко переносите узлы между документами с помощью метода ImportNode от NodeImporter. Улучшите свой рабочий процесс и оптимизируйте интеграцию данных уже сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

Импортирует узел из одного документа в другой.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | Node | Узел для импорта. |
| isImportChildren | Boolean | `истинный` для рекурсивного импорта всех дочерних узлов; в противном случае,`ЛОЖЬ`. |

### Возвращаемое значение

Клонированный импортированный узел. Узел принадлежит целевому документу, но не имеет родителя.

## Примечания

Импорт узла создает копию исходного узла, принадлежащего импортирующему документу. Возвращенный узел не имеет родителя. Исходный узел не изменяется и не удаляется из исходного документа.

Прежде чем узел из другого документа может быть вставлен в этот документ, он должен быть импортирован. Во время импорта специфические для документа свойства, такие как ссылки на стили и списки, транслируются из исходного в импортирующий документ. После импорта узла его можно вставить в соответствующее место в документе с помощью[`InsertBefore`](../../compositenode/insertbefore/) или [`InsertAfter`](../../compositenode/insertafter/).

Если исходный узел уже принадлежит целевому документу, то просто создается глубокий клон исходного узла.

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

* class [Node](../../node/)
* class [NodeImporter](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
