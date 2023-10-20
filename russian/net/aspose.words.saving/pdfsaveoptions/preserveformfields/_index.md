---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words для .NET
description: PdfSaveOptions PreserveFormFields свойство. Указывает следует ли сохранять поля формы Microsoft Word как поля формы в PDF или преобразовывать их в текст. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 270
url: /ru/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Указывает, следует ли сохранять поля формы Microsoft Word как поля формы в PDF или преобразовывать их в текст. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Примечания

Поля формы Microsoft Word включают в себя ввод текста, раскрывающийся список и элементы управления флажками.

Если установлено значение`ЛОЖЬ` , эти поля будут экспортированы как текст в PDF. Если установлено значение`истинный`, эти поля будут экспортированы как поля формы PDF.

При экспорте полей формы в PDF в качестве полей формы могут возникнуть некоторые потери форматирования, поскольку поля PDF form не поддерживают все функции полей формы Microsoft Word.

Кроме того, размер вывода зависит от размера содержимого, поскольку редактируемые формы в Microsoft Word представляют собой встроенные объекты .

Редактируемые формы запрещены стандартом PDF/A.`ЛОЖЬ` значение будет использоваться автоматически при сохранении в PDF/A.

Поля формы не поддерживаются при сохранении в PDF/UA.`ЛОЖЬ` значение будет использовано автоматически.

## Примеры

Показывает, как сохранить документ в формате PDF с помощью метода Save и класса PdfSaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Вставляем поле со списком, которое позволит пользователю выбрать вариант из коллекции строк.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Установите для свойства PreserveFormFields значение «true», чтобы сохранить поля формы как интерактивные объекты в выходном PDF-файле.
// Установите для свойства PreserveFormFields значение «false», чтобы заморозить все поля формы в документе на
// их текущие значения и отображаем их в виде обычного текста в выходном PDF-файле.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
