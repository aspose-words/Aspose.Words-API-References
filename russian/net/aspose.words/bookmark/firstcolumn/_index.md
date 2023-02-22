---
title: Bookmark.FirstColumn
second_title: Справочник по API Aspose.Words для .NET
description: Bookmark свойство. Получает отсчитываемый от нуля индекс первого столбца диапазона столбцов таблицы связанного с закладкой.
type: docs
weight: 30
url: /ru/net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

Получает отсчитываемый от нуля индекс первого столбца диапазона столбцов таблицы, связанного с закладкой.

```csharp
public int FirstColumn { get; }
```

### Примечания

Возвращает **-1** если эта закладка не является закладкой столбца таблицы.

### Примеры

Показывает, как получить информацию о закладках столбца таблицы.

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
            // Печатаем содержимое первой и последней колонок, заключенных в закладку.
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


