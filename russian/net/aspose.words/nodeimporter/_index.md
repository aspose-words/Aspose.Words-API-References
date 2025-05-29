---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words для .NET
description: Легко переносите узлы документов с помощью Aspose.Words.NodeImporter. Оптимизируйте свой рабочий процесс и повысьте эффективность управления документами уже сегодня!
type: docs
weight: 4900
url: /ru/net/aspose.words/nodeimporter/
---
## NodeImporter class

Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public class NodeImporter
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Инициализирует новый экземпляр`NodeImporter` класс. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Инициализирует новый экземпляр`NodeImporter` класс. |

## Методы

| Имя | Описание |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Импортирует узел из одного документа в другой. |

## Примечания

Aspose.Words предоставляет функциональность для простого копирования и перемещения фрагментов между документами Microsoft Word. Это известно как «импорт узлов». Прежде чем вставить фрагмент из одного документа в другой, его необходимо «импортировать». Импорт создает глубокий клон исходного узла, готовый к вставке в целевой документ .

Самый простой способ импортировать узел — использовать[`ImportNode`](../documentbase/importnode/) method предоставленный[`DocumentBase`](../documentbase/) объект.

Однако, когда вам нужно импортировать узлы из одного документа в другой несколько раз, лучше использовать`NodeImporter` класс.`NodeImporter` Класс позволяет минимизировать количество стилей и списков, создаваемых в целевом документе.

Копирование или перемещение фрагментов из одного документа Microsoft Word в другой представляет собой number технических проблем для Aspose.Words. В документе Word стили и форматирование списков хранятся централизованно, отдельно от текста документа. Абзацы и фрагменты текста просто ссылаются на стили с помощью внутренних уникальных идентификаторов.

Проблемы возникают из-за того, что стили и списки в разных документах различаются. Например, чтобы скопировать абзац, отформатированный с помощью стиля «Заголовок 1», из одного документа в другой, необходимо учесть ряд факторов: решить, копировать ли стиль «Заголовок 1» из исходного документа в целевой документ, клонировать абзац, обновить клонированный абзац так, чтобы он ссылался на правильный стиль «Заголовок 1» в целевом документе. Если бы стиль пришлось скопировать, все стили, на которые он ссылается (на основе стиля «x000d» и стиля следующего абзаца), следует проанализировать и, возможно, также скопировать и т. д. Аналогичные проблемы возникают при копировании маркированных или нумерованных абзацев, поскольку Microsoft Word хранит определения списков отдельно от текста.

The`NodeImporter`класс подобен контексту, который содержит "таблицы перевода" во время импорта. Он корректно переводит между стилями и списками в исходном и документах назначения.

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
