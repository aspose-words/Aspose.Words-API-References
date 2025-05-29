---
title: FootnoteNumberingRule Enum
linktitle: FootnoteNumberingRule
articleTitle: FootnoteNumberingRule
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words FootnoteNumberingRule для управления автоматической нумерацией сносок и концевых сносок. Оптимизируйте форматирование документа без усилий!
type: docs
weight: 4960
url: /ru/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

Определяет, когда автоматическая нумерация сносок или концевых сносок перезапускается.

```csharp
public enum FootnoteNumberingRule
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Continuous | `0` | Нумерация сплошная по всему документу. |
| RestartSection | `1` | Нумерация начинается заново в каждом разделе. |
| RestartPage | `2` | Нумерация начинается заново на каждой странице. Действительно только для сносок. |
| Default | `0` | РавноContinuous . |

## Примеры

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

* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)
* пространство имен [Aspose.Words.Notes](../../aspose.words.notes/)
* сборка [Aspose.Words](../../)
