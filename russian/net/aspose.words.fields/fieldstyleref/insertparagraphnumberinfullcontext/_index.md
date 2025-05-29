---
title: FieldStyleRef.InsertParagraphNumberInFullContext
linktitle: InsertParagraphNumberInFullContext
articleTitle: InsertParagraphNumberInFullContext
second_title: Aspose.Words для .NET
description: Управляйте нумерацией абзацев с помощью свойства FieldStyleRef InsertParagraphNumberInFullContext. Легко управляйте контекстом для большей ясности документа.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext/
---
## FieldStyleRef.InsertParagraphNumberInFullContext property

Возвращает или задает, следует ли вставлять номер абзаца, на который ссылаются, в полном контексте.

```csharp
public bool InsertParagraphNumberInFullContext { get; set; }
```

## Примеры

Показывает, как использовать поля STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте список на основе шаблона списка Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Этот сгенерированный список будет отображать «1.a )».
 // Пробел перед скобкой — это не разделительный символ, который мы можем подавить.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Добавьте текст и примените стили абзацев, на которые будут ссылаться поля STYLEREF.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Размещаем поле STYLEREF в заголовке и отображаем первый текст в стиле «Абзац списка» в документе.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Поместите поле STYLEREF в нижний колонтитул и отобразите в нем последний текст.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Мы также можем использовать поля STYLEREF для ссылки на номера списков.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Смотрите также

* class [FieldStyleRef](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
