---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words для .NET
description: Используйте метод StartColumnBookmark в DocumentBuilder, чтобы легко отмечать позиции ячеек таблицы в качестве закладок столбцов, улучшая навигацию и организацию документа.
type: docs
weight: 660
url: /ru/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Отмечает текущую позицию в документе как начало закладки столбца. Позиция должна быть в ячейке таблицы.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Название закладки. |

### Возвращаемое значение

Начальный узел закладки, который был только что создан.

## Примечания

Закладка столбца охватывает один или несколько столбцов в диапазоне строк. Чтобы создать действительную закладку you нужно вызвать оба`StartColumnBookmark` и[`EndColumnBookmark`](../endcolumnbookmark/) с тем же *bookmarkName* параметр.

Неправильно сформированные закладки или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

Фактическое положение вставленного[`BookmarkStart`](../../bookmarkstart/) узел может отличаться от текущей позиции document builder.

## Примеры

Показывает, как создать закладку столбца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Ячейки 1,2,4,5 будут добавлены в закладки.
builder.StartColumnBookmark("MyBookmark_1");
// Неправильно сформированные закладки или закладки с повторяющимися именами будут игнорироваться при сохранении документа.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
