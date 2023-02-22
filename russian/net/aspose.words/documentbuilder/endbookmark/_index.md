---
title: DocumentBuilder.EndBookmark
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Помечает текущую позицию в документе как конец закладки.
type: docs
weight: 190
url: /ru/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

Помечает текущую позицию в документе как конец закладки.

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Название закладки. |

### Возвращаемое значение

Только что созданный конечный узел закладки.

### Примечания

Закладки в документе могут перекрываться и охватывать любой диапазон. Чтобы создать действительную закладку, вам нужно вызвать оба[`StartBookmark`](../startbookmark/) а также`EndBookmark` с тем же **bookmarkName** параметр.

Неправильно сформированные закладки или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

### Примеры

Показывает, как создать закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Действительная закладка должна иметь основной текст документа, заключенный в
// Созданы узлы BookmarkStart и BookmarkEnd с совпадающим именем закладки.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Показывает, как вставить гиперссылку, ссылающуюся на локальную закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Вставьте поле ГИПЕРССЫЛКИ, которое ссылается на закладку. Мы можем передать полевые переключатели
// в метод "InsertHyperlink" как часть аргумента, содержащего имя закладки, на которую делается ссылка.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Смотрите также

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


