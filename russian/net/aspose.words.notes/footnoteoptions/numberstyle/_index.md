---
title: FootnoteOptions.NumberStyle
second_title: Справочник по API Aspose.Words для .NET
description: FootnoteOptions свойство. Определяет числовой формат для автоматически нумерованных сносок.
type: docs
weight: 20
url: /ru/net/aspose.words.notes/footnoteoptions/numberstyle/
---
## FootnoteOptions.NumberStyle property

Определяет числовой формат для автоматически нумерованных сносок.

```csharp
public NumberStyle NumberStyle { get; set; }
```

### Примечания

Не все стили номеров применимы для этого свойства. Список применимых стилей чисел см. в диалоговом окне «Вставить сноску» или «Концевую сноску» в Microsoft Word. Если вы выберете стиль чисел, который неприменим, Microsoft Word вернется к значению по умолчанию.

### Примеры

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

### Смотрите также

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [FootnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../footnoteoptions/)
* сборка [Aspose.Words](../../../)


