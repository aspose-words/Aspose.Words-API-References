---
title: Bookmark.IsColumn
linktitle: IsColumn
articleTitle: IsColumn
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsColumn. Легко определите, представляет ли закладка столбец таблицы, что улучшит навигацию и организацию документа.
type: docs
weight: 40
url: /ru/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Возврат`истинный` если эта закладка является закладкой столбца таблицы.

```csharp
public bool IsColumn { get; }
```

## Примеры

Показывает, как получить информацию о закладках столбцов таблицы.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Если закладка охватывает столбцы таблицы, то это закладка столбца таблицы, и ее флаг IsColumn имеет значение true.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Распечатать содержимое первого и последнего столбцов, заключенных в закладку.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Смотрите также

* class [Bookmark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
