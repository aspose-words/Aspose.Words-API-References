---
title: NodeImporter
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.
type: docs
weight: 3920
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
| [NodeImporter](nodeimporter#constructor)(DocumentBase, DocumentBase, ImportFormatMode) | Инициализирует новый экземпляр класса[`NodeImporter`](../nodeimporter). |
| [NodeImporter](nodeimporter#constructor_1)(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) | Инициализирует новый экземпляр класса[`NodeImporter`](../nodeimporter). |

## Методы

| Имя | Описание |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode)(Node, bool) | Импорт узла из одного документа в другой. |

### Примечания

Aspose.Words предоставляет функциональность для простого копирования и перемещения фрагментов между Документы Microsoft Word. Это известно как «импорт узлов». Прежде чем вставить фрагмент из одного документа в другой, его нужно "импортировать". Импорт создает глубокий клон исходного узла, готовый к вставке в целевой документ .

Самый простой способ импортировать узел — использовать метод[`ImportNode`](../documentbase/importnode)метод предоставленный объектом[`DocumentBase`](../documentbase).

Однако, когда вам нужно несколько раз импортировать узлы из одного документа в другой, лучше использовать[`NodeImporter`](../nodeimporter)класс. Класс[`NodeImporter`](../nodeimporter) позволяет минимизировать количество стилей и списков, создаваемых в целевом документе.

Копирование или перемещение фрагментов из одного документа Microsoft Word в другой представляет собой ряд технических проблем для Aspose.Words. В документе Word стили и форматирование списка хранятся централизованно, отдельно от текста документа. Абзацы и фрагменты текста просто ссылаются на стили по внутренним уникальным идентификаторам.

Проблемы возникают из-за того, что стили и списки различаются в разных документах. Например, чтобы скопировать абзац, оформленный в стиле Заголовок 1, из одного документа в другой, необходимо принять во внимание ряд вещей:решить, следует ли копировать Заголовок 1 стиль из исходного документа в целевой документ, клонировать абзац, обновить клонированный абзац так, чтобы он ссылался на правильный стиль заголовка 1 в целевом документе. Если стиль должен быть скопирован, все стили, на которые он ссылается (на основе стиля и стиля следующего абзаца), должны быть проанализированы и, возможно, скопированы, и так далее. Аналогичные проблемы возникают при копировании маркированных или пронумерованных абзацев, поскольку Microsoft Word хранит определения списков отдельно от текста.

Класс[`NodeImporter`](../nodeimporter)подобен контексту, который содержит "таблицы перевода" во время импорта. Он корректно переводит стили и списки в исходный и конечный документы.

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

         // Перебираем все узлы блочного уровня в теле раздела, 
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

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
