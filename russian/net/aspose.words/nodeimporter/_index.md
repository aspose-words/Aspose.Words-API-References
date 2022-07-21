---
title: NodeImporter
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.
type: docs
weight: 3970
url: /ru/net/aspose.words/nodeimporter/
---
## NodeImporter class

Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.

```csharp
public class NodeImporter
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [NodeImporter](nodeimporter#constructor)(DocumentBase, DocumentBase, ImportFormatMode) | Инициализирует новый экземпляр[`NodeImporter`](../nodeimporter) класс. |
| [NodeImporter](nodeimporter#constructor_1)(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) | Инициализирует новый экземпляр[`NodeImporter`](../nodeimporter) класс. |

## Методы

| Имя | Описание |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode)(Node, bool) | Импортирует узел из одного документа в другой. |

### Примечания

Aspose.Words предоставляет функциональные возможности для простого копирования и перемещения фрагментов между документами Microsoft Word. Это известно как «импорт узлов». Прежде чем вы сможете вставить фрагмент из одного документа в другой, его необходимо «импортировать».

Самый простой способ импортировать узел — использовать[`ImportNode`](../documentbase/importnode) method предоставленный[`DocumentBase`](../documentbase) объект.

Однако, когда вам нужно несколько раз импортировать узлы из одного документа в другой, лучше использовать[`NodeImporter`](../nodeimporter) учебный класс.[`NodeImporter`](../nodeimporter) Класс позволяет минимизировать количество стилей и списков, создаваемых в целевом документе.

Копирование или перемещение фрагментов из одного документа Microsoft Word в другой представляет собой число технических проблем для Aspose.Words. В документе Word стили и список formatting хранятся централизованно, отдельно от текста документа. Параграфы и фрагменты текста просто ссылаются на стили по внутренним уникальным идентификаторам.

Проблемы возникают из-за того, что стили и списки различаются в разных документах. Например, чтобы скопировать абзац, отформатированный в стиле «Заголовок 1», из одного документа в другой, необходимо принять во внимание ряд факторов: решить, следует ли скопируйте стиль заголовка 1 из исходного документа в целевой документ, клонируйте абзац, обновите абзац cloned , чтобы он ссылался на правильный стиль заголовка 1 в целевом документе. ссылки (на основе style и стиля следующего абзаца) должны быть проанализированы и, возможно, скопированы, и т. д. Аналогичные проблемы возникают при копировании маркированных или пронумерованных абзацев, поскольку Microsoft Word хранит определения списков отдельно от текста.

[`NodeImporter`](../nodeimporter)class подобен контексту, который содержит "таблицы перевода" во время импорта. Он корректно переводит стили и списки в исходный и конечный документы.

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

* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
