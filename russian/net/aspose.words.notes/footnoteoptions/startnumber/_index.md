---
title: FootnoteOptions.StartNumber
second_title: Справочник по API Aspose.Words для .NET
description: FootnoteOptions свойство. Определяет начальный номер или символ для первых автоматически нумерованных сносок.
type: docs
weight: 50
url: /ru/net/aspose.words.notes/footnoteoptions/startnumber/
---
## FootnoteOptions.StartNumber property

Определяет начальный номер или символ для первых автоматически нумерованных сносок.

```csharp
public int StartNumber { get; set; }
```

### Примечания

Это свойство действует только тогда, когда[`RestartRule`](../restartrule/) установлен на Continuous.

### Примеры

Показывает, как установить число, с которого в документе начинается счетчик сносок/концевых сносок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноски и концевые сноски — это способ прикрепить ссылку или комментарий к тексту
// это не мешает потоку основного текста. 
// При вставке сноски/концевой сноски добавляется маленький символ надстрочной ссылки
// в основном тексте, где мы вставляем сноску/концевую сноску.
// Каждая сноска/концевая сноска также создает запись, состоящую из символа
// который соответствует ссылочному символу в основном тексте.
// Ссылочный текст, который мы передаем методу "InsertEndnote" построителя документа.
// Записи сносок по умолчанию отображаются внизу каждой страницы, содержащей
// их ссылочные символы и концевые сноски отображаются в конце документа.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// По умолчанию ссылочным символом для каждой сноски и концевой сноски является ее индекс
// среди всех сносок/концевых сносок документа. Каждый документ ведет отдельные счета
// для сносок и концевых сносок, которые начинаются с 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Мы можем использовать свойство "StartNumber", чтобы получить документ
// начинать счетчик сносок или концевых сносок с другого номера.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### Смотрите также

* class [FootnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../footnoteoptions/)
* сборка [Aspose.Words](../../../)


