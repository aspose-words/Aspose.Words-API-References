---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words для .NET
description: Узнайте, как свойство EndnoteOptions Position улучшает макет вашего документа, указывая идеальное размещение концевых сносок. Оптимизируйте свой текст сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Указывает положение концевых сносок.

```csharp
public EndnotePosition Position { get; set; }
```

## Примеры

Показывает, как выбрать другое место, где документ собирает и отображает свои концевые сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноска — это способ прикрепить ссылку или боковой комментарий к тексту.
 // это не мешает потоку основного текста.
// Вставка концевой сноски добавляет небольшой верхний индексный символ ссылки
// в основном тексте, где мы вставляем концевую сноску.
// Каждая концевая сноска также создает запись в конце документа, состоящую из символа
// который соответствует ссылочному символу в основном тексте.
// Текст ссылки, который мы передаем методу "InsertEndnote" конструктора документов.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Мы можем использовать свойство «Position», чтобы определить, где в документе будут размещены все концевые сноски.
// Если мы установим значение свойства "Position" на "EndnotePosition.EndOfDocument",
// каждая сноска будет отображаться в коллекции в конце документа. Это значение по умолчанию.
// Если мы установим значение свойства "Position" на "EndnotePosition.EndOfSection",
// каждая сноска будет отображаться в коллекции в конце раздела, текст которого содержит ссылочный знак концевой сноски.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Смотрите также

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
