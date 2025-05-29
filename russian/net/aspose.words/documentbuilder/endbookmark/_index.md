---
title: DocumentBuilder.EndBookmark
linktitle: EndBookmark
articleTitle: EndBookmark
second_title: Aspose.Words для .NET
description: С легкостью отмечайте конец закладки в документе с помощью метода EndBookmark в DocumentBuilder, улучшая организацию документа и навигацию по нему.
type: docs
weight: 210
url: /ru/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

Отмечает текущую позицию в документе как конец закладки.

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Название закладки. |

### Возвращаемое значение

Конечный узел закладки, который был только что создан.

## Примечания

Закладки в документе могут перекрываться и охватывать любой диапазон. Чтобы создать действительную закладку, вам нужно вызвать to оба[`StartBookmark`](../startbookmark/) и`EndBookmark` с тем же самым*bookmarkName* Параметр .

Неправильно сформированные закладки или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

## Примеры

Показывает, как создать закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Действительная закладка должна иметь текст документа, заключенный в
// Узлы BookmarkStart и BookmarkEnd созданы с соответствующим именем закладки.
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

// Вставьте поле HYPERLINK, которое ссылается на закладку. Мы можем передавать переключатели полей
// в метод "InsertHyperlink" как часть аргумента, содержащего имя указанной закладки.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Смотрите также

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
