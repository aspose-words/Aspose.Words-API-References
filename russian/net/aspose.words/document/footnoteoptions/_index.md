---
title: Document.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words для .NET
description: Изучите свойство Document FootnoteOptions, чтобы настроить нумерацию и расположение сносок, повысив ясность и профессионализм вашего документа.
type: docs
weight: 160
url: /ru/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

Предоставляет параметры, управляющие нумерацией и расположением сносок в этом документе.

```csharp
public FootnoteOptions FootnoteOptions { get; }
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

Показывает, как задать номер, с которого в документе начинается отсчет сносок/концевых сносок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноски и концевые сноски — это способ прикрепить ссылку или боковой комментарий к тексту.
 // это не мешает потоку основного текста.
// Вставка сноски/концевой сноски добавляет небольшой надстрочный символ ссылки
// в основном тексте, где мы вставляем сноску/концевую сноску.
// Каждая сноска/концевая сноска также создает запись, которая состоит из символа
// который соответствует ссылочному символу в основном тексте.
// Текст ссылки, который мы передаем методу "InsertEndnote" конструктора документов.
// Сноски по умолчанию отображаются внизу каждой страницы, содержащей
// их справочные символы и концевые сноски отображаются в конце документа.
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

// По умолчанию символом ссылки для каждой сноски и концевой сноски является ее индекс
// среди всех сносок/концевых сносок документа. Каждый документ ведет отдельный подсчет
// для сносок и концевых сносок, которые начинаются с 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Мы можем использовать свойство "StartNumber", чтобы получить документ
// начать подсчет сносок или концевых сносок с другого номера.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Показывает, как изменить стиль нумерации сносок/концевых сносок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноски и концевые сноски — это способ прикрепить ссылку или боковой комментарий к тексту.
 // это не мешает потоку основного текста.
// Вставка сноски/концевой сноски добавляет небольшой надстрочный символ ссылки
// в основном тексте, где мы вставляем сноску/концевую сноску.
// Каждая сноска/концевая сноска также создает запись, которая состоит из символа, соответствующего ссылке
// символ в основном тексте. Ссылочный текст, который мы передаем в метод "InsertEndnote" конструктора документа.
// Сноски по умолчанию отображаются внизу каждой страницы, содержащей
// их справочные символы и концевые сноски отображаются в конце документа.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// По умолчанию символом ссылки для каждой сноски и концевой сноски является ее индекс
// среди всех сносок/концевых сносок документа. Каждый документ ведет отдельный подсчет
// для сносок и концевых сносок. По умолчанию сноски отображают свои номера арабскими цифрами,
// и концевые сноски отображают свои номера строчными римскими цифрами.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Мы можем использовать свойство «NumberStyle» для применения пользовательских стилей нумерации к сноскам и концевым сноскам.
// Это не повлияет на сноски/концевые сноски с пользовательскими справочными знаками.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Показывает, как перезапустить нумерацию сносок/концевых сносок в определенных местах документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноски и концевые сноски — это способ прикрепить ссылку или боковой комментарий к тексту.
 // это не мешает потоку основного текста.
// Вставка сноски/концевой сноски добавляет небольшой надстрочный символ ссылки
// в основном тексте, где мы вставляем сноску/концевую сноску.
// Каждая сноска/концевая сноска также создает запись, которая состоит из символа, соответствующего ссылке
// символ в основном тексте. Ссылочный текст, который мы передаем в метод "InsertEndnote" конструктора документа.
// Сноски по умолчанию отображаются внизу каждой страницы, содержащей
// их справочные символы и концевые сноски отображаются в конце документа.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// По умолчанию символом ссылки для каждой сноски и концевой сноски является ее индекс
// среди всех сносок/концевых сносок документа. Каждый документ ведет отдельный подсчет
// для обычных и концевых сносок и не перезапускает эти подсчеты ни в какой точке.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Мы можем использовать свойство "RestartRule", чтобы перезапустить документ
// сноска/концевая сноска считается новой страницей или разделом.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Смотрите также

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
