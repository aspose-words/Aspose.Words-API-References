---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions AdditionalTextPositioning для управления позиционированием текста в PDF-файлах. Улучшите макет вашего документа без усилий!
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Флаг, указывающий, следует ли записывать дополнительные операторы позиционирования текста или нет.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Примечания

Если`истинный` , в выходной PDF записываются дополнительные операторы позиционирования текста. Это может помочь преодолеть проблемы с неточным позиционированием текста на некоторых принтерах. Недостатком является увеличение размера документа PDF.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Покажите, как писать дополнительные операторы позиционирования текста.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Установите свойство "AdditionalTextPositioning" в значение "true", чтобы попытаться исправить неверные
    // позиционирование элементов в выходном PDF-файле, если таковые имеются, за счет увеличения размера файла.
    // Установите свойство "AdditionalTextPositioning" в значение "false", чтобы отобразить документ как обычно.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
