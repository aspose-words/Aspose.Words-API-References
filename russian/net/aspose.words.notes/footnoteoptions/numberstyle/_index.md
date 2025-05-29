---
title: FootnoteOptions.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FootnoteOptions NumberStyle, позволяющее легко настраивать форматы нумерации сносок для повышения ясности и профессионализма документа.
type: docs
weight: 20
url: /ru/net/aspose.words.notes/footnoteoptions/numberstyle/
---
## FootnoteOptions.NumberStyle property

Указывает формат номера для автоматически нумеруемых сносок.

```csharp
public NumberStyle NumberStyle { get; set; }
```

## Примечания

Не все стили чисел применимы для этого свойства. Список применимых стилей чисел см. в диалоговом окне Вставить сноску или концевую сноску в Microsoft Word. Если выбрать стиль чисел, который неприменим, Microsoft Word вернется к значению по умолчанию.

## Примеры

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

### Смотрите также

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [FootnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
