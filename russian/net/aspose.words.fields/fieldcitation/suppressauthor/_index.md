---
title: FieldCitation.SuppressAuthor
linktitle: SuppressAuthor
articleTitle: SuppressAuthor
second_title: Aspose.Words для .NET
description: Контролируйте видимость автора с помощью свойства FieldCitation SuppressAuthor. Легко управляйте данными цитирования для большей ясности и профессионализма.
type: docs
weight: 80
url: /ru/net/aspose.words.fields/fieldcitation/suppressauthor/
---
## FieldCitation.SuppressAuthor property

Возвращает или задает, будет ли информация об авторе скрыта из цитаты.

```csharp
public bool SuppressAuthor { get; set; }
```

## Примеры

Показывает, как работать с полями ЦИТАТА и БИБЛИОГРАФИЯ.

```csharp
// Открываем документ, содержащий библиографические источники, которые мы можем найти в
// Microsoft Word через Ссылки -> Цитаты и библиография -> Управление источниками.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Создайте ссылку, указав только номер страницы и автора указанной книги.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Мы ссылаемся на источники, используя их имена тегов.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Создайте более подробную цитату, ссылающуюся на два источника.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Мы можем использовать поле БИБЛИОГРАФИЯ для отображения всех источников в документе.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Смотрите также

* class [FieldCitation](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
