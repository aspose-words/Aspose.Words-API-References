---
title: PdfSaveOptions.AdditionalTextPositioning
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Флаг определяющий писать ли дополнительные операторы позиционирования текста или нет.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Флаг, определяющий, писать ли дополнительные операторы позиционирования текста или нет.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

### Примечания

Если`истинный` , в выходной PDF-файл записываются дополнительные операторы позиционирования текста. Это может помочь решить проблемы с неточным позиционированием текста на некоторых принтерах. Обратной стороной является увеличенный размер PDF-документа.

Значение по умолчанию:`ЛОЖЬ`.

### Примеры

Покажите, как писать дополнительные операторы позиционирования текста.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Установите для свойства «AdditionalTextPositioning» значение «true», чтобы попытаться исправить неправильные
    // позиционирование элемента в выходном PDF-файле, если таковой имеется, за счет увеличения размера файла.
    // Установите для свойства «AdditionalTextPositioning» значение «false», чтобы отобразить документ как обычно.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


