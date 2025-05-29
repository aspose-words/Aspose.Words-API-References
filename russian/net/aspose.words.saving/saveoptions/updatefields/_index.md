---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SaveOptions UpdateFields оптимизирует сохранение документа путем обновления определенных типов полей перед преобразованием в фиксированные форматы. По умолчанию — true.
type: docs
weight: 170
url: /ru/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Возвращает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства:`истинный` .

```csharp
public bool UpdateFields { get; set; }
```

## Примечания

Позволяет указать, имитировать ли поведение MS Word.

## Примеры

Показывает, как обновить все поля в документе непосредственно перед его сохранением в формате PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте текст с полями PAGE и NUMPAGES. Эти поля не отображают правильное значение в реальном времени.
// Нам нужно будет вручную обновить их, используя методы обновления, такие как "Field.Update()" и "Document.UpdateFields()"
// каждый раз нам нужно, чтобы они отображали точные значения.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство «UpdateFields» в значение «false», чтобы не обновлять все поля в документе непосредственно перед операцией сохранения.
// Это предпочтительный вариант, если мы знаем, что все наши поля будут обновлены перед сохранением.
// Установите свойство "UpdateFields" в значение "true", чтобы выполнить итерацию по всему документу
// поля и обновить их перед сохранением в формате PDF. Это гарантирует, что все поля будут отображаться
// самые точные значения в PDF.
options.UpdateFields = updateFields;

// Мы можем клонировать объекты PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
