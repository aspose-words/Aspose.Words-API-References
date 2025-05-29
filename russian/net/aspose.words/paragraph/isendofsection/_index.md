---
title: Paragraph.IsEndOfSection
linktitle: IsEndOfSection
articleTitle: IsEndOfSection
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Paragraph IsEndOfSection, определите, является ли абзац последним в основном тексте раздела, для улучшения структуры документа и ясности.
type: docs
weight: 80
url: /ru/net/aspose.words/paragraph/isendofsection/
---
## Paragraph.IsEndOfSection property

Истина, если этот абзац является последним абзацем в[`Body`](../../body/) (основной текст рассказа)[`Section`](../../section/) ; в противном случае ложно.

```csharp
public bool IsEndOfSection { get; }
```

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

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
