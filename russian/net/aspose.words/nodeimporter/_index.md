---
title: Class NodeImporter
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.NodeImporter сорт. Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.
type: docs
weight: 4210
url: /ru/net/aspose.words/nodeimporter/
---
## NodeImporter class

Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) статья документации.

```csharp
public class NodeImporter
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(DocumentBase, DocumentBase, ImportFormatMode) | Инициализирует новый экземпляр`NodeImporter` класс. |
| [NodeImporter](nodeimporter/#constructor_1)(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) | Инициализирует новый экземпляр`NodeImporter` класс. |

## Методы

| Имя | Описание |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(Node, bool) | Импортирует узел из одного документа в другой. |

### Примечания

Aspose.Words предоставляет функциональные возможности для простого копирования и перемещения фрагментов между документами Microsoft Word. Это называется «импортом узлов». Прежде чем вы сможете вставить фрагмент из одного документа в другой, вам необходимо «импортировать» его. При импорте создается глубокий клон исходного узла, готовый к вставке в целевой документ .

Самый простой способ импортировать узел — использовать команду[`ImportNode`](../documentbase/importnode/) метод предоставлен[`DocumentBase`](../documentbase/) объект.

Однако, когда вам нужно несколько раз импортировать узлы из одного документа в другой, лучше использовать`NodeImporter` сорт.`NodeImporter` Класс позволяет минимизировать количество стилей и списков, создаваемых в целевом документе.

Копирование или перемещение фрагментов из одного документа Microsoft Word в другой представляет собой количество технических проблем для Aspose.Words. В документе Word стили и форматирование списка хранятся централизованно, отдельно от текста документа. Параграфы и фрагменты текста просто ссылаются на стили посредством внутренних уникальных идентификаторов.

Проблемы возникают из-за того, что стили и списки в разных документах различаются. Например, чтобы скопировать абзац, отформатированный со стилем «Заголовок 1», из одного документа в другой, необходимо принять во внимание ряд вещей: решить, следует ли скопируйте стиль заголовка 1 из исходного документа в целевой документ, клонируйте абзац, обновите абзац cloned , чтобы он ссылался на правильный стиль заголовка 1 в целевом документе. Если стиль нужно было скопировать, все стили, которые он ссылки (на основе style и стиля следующего абзаца) должны быть проанализированы и, возможно, также скопированы и т. д. Аналогичные проблемы возникают при копировании маркированных или нумерованных абзацев, поскольку Microsoft Word хранит определения списков отдельно от текста.

`NodeImporter`класс подобен контексту, который содержит «таблицы перевода» во время импорта. Он правильно преобразует стили и списки в исходных и целевых документах.

### Примеры

Показывает, как вставить содержимое одного документа в закладку в другом документе.

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
        // затем клонируем и вставляем каждый узел, кроме последнего пустого абзаца раздела.
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


