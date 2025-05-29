---
title: BookmarkEnd Class
linktitle: BookmarkEnd
articleTitle: BookmarkEnd
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.BookmarkEnd, который эффективно управляет концами закладок в документах Word, улучшая процесс редактирования документов.
type: docs
weight: 250
url: /ru/net/aspose.words/bookmarkend/
---
## BookmarkEnd class

Обозначает конец закладки в документе Word.

Чтобы узнать больше, посетите[Работа с закладками](https://docs.aspose.com/words/net/working-with-bookmarks/) документальная статья.

```csharp
public class BookmarkEnd : Node
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [BookmarkEnd](bookmarkend/)(*[DocumentBase](../documentbase/), string*) | Инициализирует новый экземпляр`BookmarkEnd` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возврат`истинный` если этот узел может содержать другие узлы. |
| [Name](../../aspose.words/bookmarkend/name/) { get; set; } | Получает или задает имя закладки. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words/bookmarkend/nodetype/) { get; } | ВозвратBookmarkEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/bookmarkend/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

Полная закладка в документе Word состоит из[`BookmarkStart`](../bookmarkstart/) и соответствующий`BookmarkEnd` с тем же именем закладки.

[`BookmarkStart`](../bookmarkstart/) и`BookmarkEnd` — это всего лишь маркеры внутри document , которые указывают, где начинается и заканчивается закладка.

Используйте[`Bookmark`](../bookmark/) класс как «фасад» для работы с bookmark как с единым объектом.

## Примеры

Показывает, как добавлять закладки и обновлять их содержимое.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Создайте документ с тремя закладками, затем используйте пользовательскую реализацию посетителя документа для печати их содержимого.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Доступ к закладкам в коллекции закладок можно осуществлять по индексу или имени, а их имена можно обновлять.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Распечатайте все закладки еще раз, чтобы увидеть обновленные значения.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Создать документ с заданным количеством закладок.
/// </summary>
private static Document CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        string bookmarkName = "MyBookmark_" + i;

        builder.Write("Text before bookmark.");
        builder.StartBookmark(bookmarkName);
        builder.Write($"Text inside {bookmarkName}.");
        builder.EndBookmark(bookmarkName);
        builder.Writeln("Text after bookmark.");
    }

    return doc;
}

/// <summary>
/// Используйте итератор и посетителя для вывода информации о каждой закладке в коллекции.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Заставить каждую закладку в коллекции принять посетителя, который распечатает ее содержимое.
    using (IEnumerator<Bookmark> enumerator = bookmarks.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Bookmark currentBookmark = enumerator.Current;

            if (currentBookmark != null)
            {
                currentBookmark.BookmarkStart.Accept(bookmarkVisitor);
                currentBookmark.BookmarkEnd.Accept(bookmarkVisitor);

                Console.WriteLine(currentBookmark.BookmarkStart.GetText());
            }
        }
    }
}

/// <summary>
/// Выводит содержимое каждой посещенной закладки на консоль.
/// </summary>
public class BookmarkInfoPrinter : DocumentVisitor
{
    public override VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
    {
        Console.WriteLine($"BookmarkStart name: \"{bookmarkStart.Name}\", Contents: \"{bookmarkStart.Bookmark.Text}\"");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
    {
        Console.WriteLine($"BookmarkEnd name: \"{bookmarkEnd.Name}\"");
        return VisitorAction.Continue;
    }
}
```

### Смотрите также

* class [Node](../node/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
