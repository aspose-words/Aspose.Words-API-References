---
title: DocumentBuilder.EndColumnBookmark
linktitle: EndColumnBookmark
articleTitle: EndColumnBookmark
second_title: Aspose.Words для .NET
description: DocumentBuilder EndColumnBookmark метод. Отмечает текущую позицию в документе как конец закладки столбца. Позиция должна находиться в ячейке таблицы на С#.
type: docs
weight: 220
url: /ru/net/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder.EndColumnBookmark method

Отмечает текущую позицию в документе как конец закладки столбца. Позиция должна находиться в ячейке таблицы.

```csharp
public BookmarkEnd EndColumnBookmark(string bookmarkName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Название закладки. |

### Возвращаемое значение

Конечный узел закладки, который был только что создан.

## Примечания

Закладка столбца охватывает один или несколько столбцов в диапазоне строк. Чтобы создать действительную закладку, you необходимо вызвать оба[`StartColumnBookmark`](../startcolumnbookmark/) и`EndColumnBookmark` с тем же *bookmarkName*параметр.

Закладки неправильного формата или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

Фактическое положение вставленного[`BookmarkEnd`](../../bookmarkend/) узел может отличаться от текущей позиции компоновщика document .

## Примеры

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

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
