---
title: FootnoteOptions
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет параметры управляющие нумерацией и расположением сносок в этом документе.
type: docs
weight: 150
url: /ru/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

Предоставляет параметры, управляющие нумерацией и расположением сносок в этом документе.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

### Примеры

Показывает, как выбрать другое место, где документ будет собирать и отображать свои сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноска — это способ прикрепить ссылку или комментарий к тексту
// это не мешает потоку основного текста.  
// Вставка сноски добавляет небольшой верхний индекс ссылки
// в основном тексте, где мы вставляем сноску.
// Каждая сноска также создает запись внизу страницы, состоящую из символа
// который соответствует ссылочному символу в основном тексте.
// Ссылочный текст, который мы передаем методу "InsertFootnote" построителя документа.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Мы можем использовать свойство «Позиция», чтобы определить, где документ будет размещать все свои сноски.
// Если мы установим значение свойства "Position" в "FootnotePosition.BottomOfPage",
// каждая сноска будет отображаться внизу страницы, содержащей соответствующую метку. Это значение по умолчанию.
// Если мы установим значение свойства "Позиция" в "FootnotePosition.BeneathText",
// каждая сноска будет отображаться в конце текста страницы, содержащего ее контрольную отметку.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

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

Показывает, как изменить стиль номеров сносок/концевых сносок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноски и концевые сноски — это способ прикрепить ссылку или комментарий к тексту
// это не мешает потоку основного текста. 
// При вставке сноски/концевой сноски добавляется маленький символ надстрочной ссылки
// в основном тексте, где мы вставляем сноску/концевую сноску.
// Каждая сноска/концевая сноска также создает запись, состоящую из символа, соответствующего ссылке
// символ в основном тексте. Ссылочный текст, который мы передаем методу «InsertEndnote» конструктора документов.
// Записи сносок по умолчанию отображаются внизу каждой страницы, содержащей
// их ссылочные символы и концевые сноски отображаются в конце документа.
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

// По умолчанию ссылочным символом для каждой сноски и концевой сноски является ее индекс
// среди всех сносок/концевых сносок документа. Каждый документ ведет отдельные счета
// для сносок и концевых сносок. По умолчанию в сносках номера отображаются арабскими цифрами.
// и концевые сноски отображают свои номера строчными римскими цифрами.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Мы можем использовать свойство "NumberStyle" для применения пользовательских стилей нумерации к сноскам и концевым сноскам.
// Это не повлияет на сноски/концевые сноски с пользовательскими ссылочными метками.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Показывает, как перезапустить нумерацию сносок/концевых сносок в определенных местах документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноски и концевые сноски — это способ прикрепить ссылку или комментарий к тексту
// это не мешает потоку основного текста. 
// При вставке сноски/концевой сноски добавляется маленький символ надстрочной ссылки
// в основном тексте, где мы вставляем сноску/концевую сноску.
// Каждая сноска/концевая сноска также создает запись, состоящую из символа, соответствующего ссылке
// символ в основном тексте. Ссылочный текст, который мы передаем методу «InsertEndnote» конструктора документов.
// Записи сносок по умолчанию отображаются внизу каждой страницы, содержащей
// их ссылочные символы и концевые сноски отображаются в конце документа.
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

// По умолчанию ссылочным символом для каждой сноски и концевой сноски является ее индекс
// среди всех сносок/концевых сносок документа. Каждый документ ведет отдельные счета
// для сносок и концевых сносок и никогда не перезапускает эти счетчики.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Мы можем использовать свойство "RestartRule", чтобы перезапустить документ
// сноска/концевая сноска считается на новой странице или в разделе.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Смотрите также

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions)
* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
