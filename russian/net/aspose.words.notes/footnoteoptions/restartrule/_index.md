---
title: FootnoteOptions.RestartRule
second_title: Справочник по API Aspose.Words для .NET
description: FootnoteOptions свойство. Определяет когда перезапускается автоматическая нумерация.
type: docs
weight: 40
url: /ru/net/aspose.words.notes/footnoteoptions/restartrule/
---
## FootnoteOptions.RestartRule property

Определяет, когда перезапускается автоматическая нумерация.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

### Примеры

Показывает, как перезапустить нумерацию сносок/концевых сносок в определенных местах документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Сноски и концевые сноски – это способ прикрепить к тексту ссылку или комментарий.
 // это не мешает потоку основного текста.
// Вставка сноски/концевой сноски добавляет небольшой надстрочный символ ссылки
// в основном тексте, куда мы вставляем сноску/заключительную сноску.
// Каждая сноска/концевая сноска также создает запись, состоящую из символа, соответствующего ссылке
// символ в основном тексте. Справочный текст, который мы передаем методу компоновщика документов «InsertEndnote».
// Записи сносок по умолчанию отображаются внизу каждой страницы, содержащей
// их ссылочные символы и сноски отображаются в конце документа.
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

// По умолчанию ссылочным символом для каждой сноски и концевой сноски является их индекс
// среди всех сносок/концевых сносок документа. В каждом документе ведется отдельный учет.
// для сносок и концевых сносок и не перезапускает эти подсчеты в любой момент.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Мы можем использовать свойство RestartRule, чтобы перезапустить документ
// сноска/концевая сноска учитывается на новой странице или разделе.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Смотрите также

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [FootnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../footnoteoptions/)
* сборка [Aspose.Words](../../../)


