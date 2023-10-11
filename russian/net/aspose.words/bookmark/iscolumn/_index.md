---
title: Bookmark.IsColumn
second_title: Справочник по API Aspose.Words для .NET
description: Bookmark свойство. Возвращаетистинный если эта закладка является закладкой столбца таблицы.
type: docs
weight: 40
url: /ru/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Возвращает`истинный` если эта закладка является закладкой столбца таблицы.

```csharp
public bool IsColumn { get; }
```

### Примеры

Показывает, как получить информацию о закладках столбцов таблицы.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Если закладка охватывает столбцы таблицы, это закладка столбца таблицы, и ее флаг IsColumn установлен в значение true.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Распечатываем содержимое первого и последнего столбцов, заключенных в закладку.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Смотрите также

* class [Bookmark](../)
* пространство имен [Aspose.Words](../../bookmark/)
* сборка [Aspose.Words](../../../)


