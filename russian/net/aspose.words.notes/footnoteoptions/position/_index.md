---
title: FootnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FootnoteOptions Position улучшает макет документа, точно управляя размещением сносок для улучшения читабельности.
type: docs
weight: 30
url: /ru/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

Указывает положение сносок.

```csharp
public FootnotePosition Position { get; set; }
```

## Примеры

Показывает, как выбрать другое место, где документ собирает и отображает свои сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноска — это способ прикрепить ссылку или боковой комментарий к тексту.
 // это не мешает потоку основного текста.
// Вставка сноски добавляет небольшой верхний индексный символ ссылки
// в основном тексте, куда мы вставляем сноску.
// Каждая сноска также создает запись внизу страницы, состоящую из символа
// который соответствует ссылочному символу в основном тексте.
// Текст ссылки, который мы передаем методу "InsertFootnote" конструктора документа.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Мы можем использовать свойство «Position», чтобы определить, где в документе будут размещены все сноски.
// Если мы установим значение свойства "Position" на "FootnotePosition.BottomOfPage",
// каждая сноска будет отображаться внизу страницы, содержащей ее ссылочный знак. Это значение по умолчанию.
// Если мы установим значение свойства "Position" на "FootnotePosition.BeneathText",
// каждая сноска будет отображаться в конце текста страницы, содержащего ее сноску.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Смотрите также

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
