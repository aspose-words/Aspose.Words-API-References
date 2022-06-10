---
title: BookmarkStart
second_title: Справочник по API Aspose.Words для .NET
description: Представляет начало закладки в документе Word.
type: docs
weight: 60
url: /ru/net/aspose.words/bookmarkstart/
---
## BookmarkStart class

Представляет начало закладки в документе Word.

```csharp
public class BookmarkStart : Node
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [BookmarkStart](bookmarkstart)(DocumentBase, string) | Инициализирует новый экземпляр класса[`BookmarkStart`](../bookmarkstart). |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bookmark](../../aspose.words/bookmarkstart/bookmark) { get; } | Получает объект фасада, который инкапсулирует начало и конец этой закладки. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит данный узел. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Возвращает true, если этот узел может содержать другие узлы. |
| [Name](../../aspose.words/bookmarkstart/name) { get; set; } | Получает или задает имя закладки. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words/bookmarkstart/nodetype) { get; } | ВозвращаетBookmarkStart. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/bookmarkstart/accept)(DocumentVisitor) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| override [GetText](../../aspose.words/bookmarkstart/gettext)() | Возвращает пустую строку. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Полная закладка в документе Word состоит из[`BookmarkStart`](../bookmarkstart) и соответствующий[`BookmarkEnd`](../bookmarkend)с тем же именем закладки.

[`BookmarkStart`](../bookmarkstart)и[`BookmarkEnd`](../bookmarkend)являются просто маркерами внутри документа которые указывают, где закладка начинается и заканчивается.

Используйте класс[`Bookmark`](./bookmark)как "фасад" для работы с закладкой как единый объект.

### Примеры

Показывает, как добавлять закладки и обновлять их содержимое.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
     // Создайте документ с тремя закладками, затем используйте пользовательскую реализацию посетителя документа для печати их содержимого.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

     // Доступ к закладкам в коллекции закладок можно получить по индексу или имени, а их имена можно обновить.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

     // Печатаем все закладки еще раз, чтобы увидеть обновленные значения.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
 /// Создаем документ с заданным количеством закладок.
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
 /// Используйте итератор и посетитель для вывода информации о каждой закладке в коллекции.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Получить каждую закладку в коллекции, чтобы принять посетителя, который распечатает ее содержимое.
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

* class [Node](../node)
* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
