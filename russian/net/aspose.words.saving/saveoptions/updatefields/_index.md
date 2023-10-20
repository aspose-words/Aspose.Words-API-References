---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words для .NET
description: SaveOptions UpdateFields свойство. Получает или задает значение определяющее следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойстваистинный  на С#.
type: docs
weight: 160
url: /ru/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства:`истинный` .

```csharp
public bool UpdateFields { get; set; }
```

## Примечания

Позволяет указать, следует ли имитировать поведение MS Word.

## Примеры

Показывает, как обновить все поля в документе непосредственно перед сохранением его в PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем текст с полями PAGE и NUMPAGES. Эти поля не отображают правильное значение в реальном времени.
// Нам нужно будет обновить их вручную, используя такие методы обновления, как «Field.Update()» и «Document.UpdateFields()»
// каждый раз, когда они нужны нам для отображения точных значений.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства «UpdateFields» значение «false», чтобы не обновлять все поля в документе непосредственно перед операцией сохранения.
// Это предпочтительный вариант, если мы знаем, что все наши поля будут обновлены перед сохранением.
// Установите для свойства «UpdateFields» значение «true», чтобы перебрать весь документ
// поля и обновим их, прежде чем сохранить в формате PDF. Это обеспечит отображение всех полей.
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
