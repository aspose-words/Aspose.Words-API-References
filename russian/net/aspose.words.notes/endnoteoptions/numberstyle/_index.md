---
title: EndnoteOptions.NumberStyle
second_title: Справочник по API Aspose.Words для .NET
description: EndnoteOptions свойство. Определяет числовой формат для автоматически нумерованных сносок.
type: docs
weight: 10
url: /ru/net/aspose.words.notes/endnoteoptions/numberstyle/
---
## EndnoteOptions.NumberStyle property

Определяет числовой формат для автоматически нумерованных сносок.

```csharp
public NumberStyle NumberStyle { get; set; }
```

### Примечания

Не все числовые стили применимы к этому свойству. Список применимых стилей номеров см. в диалоговом окне «Вставка сноски» или «Конечная сноска» в Microsoft Word. Если вы выберете стиль нумерации, который неприменим, Microsoft Word вернется к значению по умолчанию.

### Примеры

Показывает, как изменить стиль нумерации сносок/заключительных сносок.

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
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// По умолчанию ссылочным символом для каждой сноски и концевой сноски является их индекс
// среди всех сносок/концевых сносок документа. В каждом документе ведется отдельный учет.
// для сносок и для концевых сносок. По умолчанию номера сносок обозначаются арабскими цифрами.
// и сноски отображают свои номера римскими цифрами в нижнем регистре.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Мы можем использовать свойство «NumberStyle» для применения пользовательских стилей нумерации к сноскам и концевым сноскам.
// Это не повлияет на сноски/концевые сноски с пользовательскими сносками.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### Смотрите также

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [EndnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../endnoteoptions/)
* сборка [Aspose.Words](../../../)


