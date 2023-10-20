---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words для .NET
description: Aspose.Words.Notes.FootnotePosition перечисление. Определяет положение сноски на С#.
type: docs
weight: 4290
url: /ru/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

Определяет положение сноски.

```csharp
public enum FootnotePosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| BottomOfPage | `1` | Сноски выводятся внизу каждой страницы. |
| BeneathText | `2` | Сноски выводятся под текстом на каждой странице. |

## Примеры

Показывает, как выбрать другое место, где документ будет собираться и отображать его сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноска — это способ прикрепить к тексту ссылку или комментарий.
 // это не мешает потоку основного текста.
// Вставка сноски добавляет небольшой надстрочный символ ссылки
// в основном тексте, куда мы вставляем сноску.
// Каждая сноска также создает запись внизу страницы, состоящую из символа
// который соответствует ссылочному символу в основном тексте.
// Текст ссылки, который мы передаем методу «InsertFootnote» компоновщика документов.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Мы можем использовать свойство «Позиция», чтобы определить, где в документе будут размещены все сноски.
// Если мы установим значение свойства «Position» в «FootnotePosition.BottomOfPage»,
// каждая сноска будет отображаться внизу страницы, содержащей соответствующий знак ссылки. Это значение по умолчанию.
// Если мы установим значение свойства «Position» в «FootnotePosition.BeneathText»,
// каждая сноска будет отображаться в конце текста страницы, содержащей соответствующий знак ссылки.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Смотрите также

* class [FootnoteOptions](../footnoteoptions/)
* пространство имен [Aspose.Words.Notes](../../aspose.words.notes/)
* сборка [Aspose.Words](../../)
