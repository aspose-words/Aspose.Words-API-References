---
title: EndnoteOptions.Position
second_title: Справочник по API Aspose.Words для .NET
description: EndnoteOptions свойство. Определяет положение концевых сносок.
type: docs
weight: 20
url: /ru/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Определяет положение концевых сносок.

```csharp
public EndnotePosition Position { get; set; }
```

### Примеры

Показывает, как выбрать другое место, где документ будет собирать и отображать концевые сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Концевая сноска — это способ прикрепить ссылку или комментарий к тексту
// это не мешает потоку основного текста. 
// Вставка концевой сноски добавляет небольшой верхний индекс ссылки
// в основном тексте, где мы вставляем концевую сноску.
// Каждая концевая сноска также создает запись в конце документа, состоящую из символа
// который соответствует ссылочному символу в основном тексте.
// Ссылочный текст, который мы передаем методу "InsertEndnote" построителя документа.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Мы можем использовать свойство «Позиция», чтобы определить, где документ будет размещать все свои концевые сноски.
// Если мы установим значение свойства "Позиция" в "EndnotePosition.EndOfDocument",
// каждая сноска будет отображаться в коллекции в конце документа. Это значение по умолчанию.
// Если мы установим значение свойства "Position" в "EndnotePosition.EndOfSection",
// каждая сноска будет отображаться в коллекции в конце раздела, текст которого содержит отметку концевой сноски.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Смотрите также

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../endnoteoptions/)
* сборка [Aspose.Words](../../../)


