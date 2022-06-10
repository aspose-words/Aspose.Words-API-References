---
title: FootnoteOptions
second_title: Справочник по API Aspose.Words для .NET
description: Представляет параметры нумерации сносок для документа или раздела.
type: docs
weight: 3990
url: /ru/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

Представляет параметры нумерации сносок для документа или раздела.

```csharp
public sealed class FootnoteOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns) { get; set; } | Указывает количество столбцов, в которых форматируется область сносок. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle) { get; set; } | Определяет числовой формат для автоматически нумерованных сносок. |
| [Position](../../aspose.words.notes/footnoteoptions/position) { get; set; } | Определяет положение сносок. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule) { get; set; } | Определяет, когда перезапускается автоматическая нумерация. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber) { get; set; } | Указывает начальный номер или символ для первых автоматически нумерованных сносок. |

### Примеры

Показывает, как разделить сноску на заданное количество столбцов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Сноски и концевые сноски — это способ прикрепить ссылку или комментарий к text
 // это не мешает потоку основного текста. 
 // Вставка сноски/концевой сноски добавляет небольшую ссылку в верхнем индексе symbol
 // в основном тексте, где мы вставляем сноску/концевую сноску.
 // Каждая сноска/концевая сноска также создает запись, которая состоит из символа, соответствующего reference
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

 // По умолчанию ссылочным символом для каждой сноски и концевой сноски является ее index
 // среди всех сносок/концевых сносок документа. Каждый документ поддерживает отдельные counts
 // для сносок и концевых сносок и никогда не перезапускает эти счетчики.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

 // Мы можем использовать свойство "RestartRule", чтобы документ перезапустился
 // сноска/концевая сноска считается на новой странице или в разделе.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

Показывает, как выбрать другое место, где документ собирает и отображает свои сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Сноски и концевые сноски — это способ прикрепить ссылку или комментарий к text
 // это не мешает потоку основного текста. 
 // Вставка сноски/концевой сноски добавляет небольшую ссылку в верхнем индексе symbol
 // в основном тексте, где мы вставляем сноску/концевую сноску.
 // Каждая сноска/концевая сноска также создает запись, которая состоит из символа, соответствующего reference
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

 // По умолчанию ссылочным символом для каждой сноски и концевой сноски является ее index
 // среди всех сносок/концевых сносок документа. Каждый документ поддерживает отдельные counts
 // для сносок и концевых сносок и никогда не перезапускает эти счетчики.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

 // Мы можем использовать свойство "RestartRule", чтобы документ перезапустился
 // сноска/концевая сноска считается на новой странице или в разделе.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

Показывает, как установить число, с которого в документе начинается счетчик сносок/концевых сносок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Сноски и концевые сноски — это способ прикрепить ссылку или комментарий к text
 // это не мешает потоку основного текста. 
 // Вставка сноски/концевой сноски добавляет небольшую ссылку в верхнем индексе symbol
 // в основном тексте, где мы вставляем сноску/концевую сноску.
 // Каждая сноска/концевая сноска также создает запись, которая состоит из символа, соответствующего reference
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

 // По умолчанию ссылочным символом для каждой сноски и концевой сноски является ее index
 // среди всех сносок/концевых сносок документа. Каждый документ поддерживает отдельные counts
 // для сносок и концевых сносок и никогда не перезапускает эти счетчики.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

 // Мы можем использовать свойство "RestartRule", чтобы документ перезапустился
 // сноска/концевая сноска считается на новой странице или в разделе.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

Показывает, как изменить стиль нумерации сноски/концевой сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Сноски и концевые сноски — это способ прикрепить ссылку или комментарий к text
 // это не мешает потоку основного текста. 
 // Вставка сноски/концевой сноски добавляет небольшую ссылку в верхнем индексе symbol
 // в основном тексте, где мы вставляем сноску/концевую сноску.
 // Каждая сноска/концевая сноска также создает запись, которая состоит из символа, соответствующего reference
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

 // По умолчанию ссылочным символом для каждой сноски и концевой сноски является ее index
 // среди всех сносок/концевых сносок документа. Каждый документ поддерживает отдельные counts
 // для сносок и концевых сносок и никогда не перезапускает эти счетчики.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

 // Мы можем использовать свойство "RestartRule", чтобы документ перезапустился
 // сноска/концевая сноска считается на новой странице или в разделе.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

Показывает, как перезапустить нумерацию сносок/концевых сносок в определенных местах документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Сноски и концевые сноски — это способ прикрепить ссылку или комментарий к text
 // это не мешает потоку основного текста. 
 // Вставка сноски/концевой сноски добавляет небольшую ссылку в верхнем индексе symbol
 // в основном тексте, где мы вставляем сноску/концевую сноску.
 // Каждая сноска/концевая сноска также создает запись, которая состоит из символа, соответствующего reference
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

 // По умолчанию ссылочным символом для каждой сноски и концевой сноски является ее index
 // среди всех сносок/концевых сносок документа. Каждый документ поддерживает отдельные counts
 // для сносок и концевых сносок и никогда не перезапускает эти счетчики.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

 // Мы можем использовать свойство "RestartRule", чтобы документ перезапустился
 // сноска/концевая сноска считается на новой странице или в разделе.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Смотрите также

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions)
* namespace [Aspose.Words.Notes](../../aspose.words.notes)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
