---
title: DocumentBuilder.StartColumnBookmark
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Отмечает текущую позицию в документе как начало закладки столбца. Позиция должна находиться в ячейке таблицы.
type: docs
weight: 630
url: /ru/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Отмечает текущую позицию в документе как начало закладки столбца. Позиция должна находиться в ячейке таблицы.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Название закладки. |

### Возвращаемое значение

Только что созданный начальный узел закладки.

### Примечания

Закладка столбца охватывает один или несколько столбцов в диапазоне строк. Чтобы создать действительную закладку, you необходимо вызвать оба`StartColumnBookmark` и[`EndColumnBookmark`](../endcolumnbookmark/) с тем же *bookmarkName*параметр.

Закладки неправильного формата или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

Фактическое положение вставленного[`BookmarkStart`](../../bookmarkstart/) узел может отличаться от текущей позиции компоновщика document .

### Примеры

Показывает, как создать закладку столбца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Ячейки 1,2,4,5 будут добавлены в закладки.
builder.StartColumnBookmark("MyBookmark_1");
// Закладки неправильного формата или закладки с повторяющимися именами будут игнорироваться при сохранении документа.
builder.StartColumnBookmark("MyBookmark_1");
builder.StartColumnBookmark("BadStartBookmark");
builder.Write("Cell 1");

builder.InsertCell();
builder.Write("Cell 2");

builder.InsertCell();
builder.Write("Cell 3");

builder.EndRow();

builder.InsertCell();
builder.Write("Cell 4");

builder.InsertCell();
builder.Write("Cell 5");
builder.EndColumnBookmark("MyBookmark_1");
builder.EndColumnBookmark("MyBookmark_1");

builder.InsertCell();
builder.Write("Cell 6");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### Смотрите также

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


