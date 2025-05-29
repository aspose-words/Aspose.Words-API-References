---
title: EndnotePosition Enum
linktitle: EndnotePosition
articleTitle: EndnotePosition
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words EndnotePosition для точного управления размещением концевых сносок в документах, расширяя возможности форматирования текста.
type: docs
weight: 4940
url: /ru/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

Определяет положение концевой сноски.

```csharp
public enum EndnotePosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| EndOfSection | `0` | Концевые сноски выводятся в конце раздела. |
| EndOfDocument | `3` | Концевые сноски выводятся в конце документа. |

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

* class [EndnoteOptions](../endnoteoptions/)
* пространство имен [Aspose.Words.Notes](../../aspose.words.notes/)
* сборка [Aspose.Words](../../)
