---
title: SaveOptions.UpdateFields
second_title: Справочник по API Aspose.Words для .NET
description: SaveOptions свойство. Получает или задает значение определяющее следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства истинный .
type: docs
weight: 170
url: /ru/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **истинный** .

```csharp
public bool UpdateFields { get; set; }
```

### Примечания

Позволяет указать, следует ли имитировать поведение MS Word.

### Примеры

Показывает, как обновить все поля в документе непосредственно перед его сохранением в формате PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставка текста с полями PAGE и NUMPAGES. Эти поля не отображают правильное значение в режиме реального времени.
// Нам нужно будет обновить их вручную, используя такие методы обновления, как "Field.Update()" и "Document.UpdateFields()"
// каждый раз, когда нам нужно, чтобы они отображали точные значения.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства "UpdateFields" значение "false", чтобы не обновлять все поля в документе непосредственно перед операцией сохранения.
// Это предпочтительный вариант, если мы знаем, что все наши поля будут обновлены перед сохранением.
// Установите для свойства "UpdateFields" значение "true", чтобы выполнить итерацию по всему документу
// поля и обновить их перед сохранением в формате PDF. Это гарантирует, что все поля будут отображаться
// самые точные значения в PDF.
options.UpdateFields = updateFields;

// Мы можем клонировать объекты PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../saveoptions/)
* сборка [Aspose.Words](../../../)


