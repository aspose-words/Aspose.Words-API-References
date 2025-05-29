---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PreserveFormFields PdfSaveOptions сохраняет поля форм Microsoft Word в PDF-файлах или преобразует их в текст. Улучшите качество вашего документа!
type: docs
weight: 280
url: /ru/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Указывает, следует ли сохранять поля формы Microsoft Word как поля формы в PDF или преобразовывать их в текст. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Примечания

Поля форм Microsoft Word включают в себя элементы управления для ввода текста, раскрывающиеся списки и флажки.

При установке на`ЛОЖЬ` , эти поля будут экспортированы как текст в PDF. Если установлено значение`истинный`, эти поля будут экспортированы как поля формы PDF.

При экспорте полей формы в PDF в качестве полей формы может произойти некоторая потеря форматирования, поскольку поля PDF form не поддерживают все функции полей формы Microsoft Word.

Кроме того, размер выходного документа зависит от размера содержимого, поскольку редактируемые формы в Microsoft Word являются встроенными объектами.

Редактируемые формы запрещены стандартом PDF/A.`ЛОЖЬ` значение будет использовано автоматически при сохранении в PDF/A.

Поля формы не поддерживаются при сохранении в PDF/UA.`ЛОЖЬ` значение будет использовано автоматически.

## Примеры

Показывает, как сохранить документ в формате PDF с помощью метода Save и класса PdfSaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Вставьте поле со списком, которое позволит пользователю выбрать вариант из набора строк.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Установите свойство «PreserveFormFields» в значение «true», чтобы сохранить поля формы как интерактивные объекты в выходном PDF-файле.
// Установите свойство "PreserveFormFields" в значение "false", чтобы заморозить все поля формы в документе
// их текущие значения и отобразить их в виде обычного текста в выходном PDF-файле.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
