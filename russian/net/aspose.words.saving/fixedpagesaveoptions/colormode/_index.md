---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FixedPageSaveOptions ColorMode для настройки цветопередачи для повышения качества документа и визуальной привлекательности. Оптимизируйте свой вывод сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Возвращает или задает значение, определяющее способ отображения цветов.

```csharp
public ColorMode ColorMode { get; set; }
```

## Примечания

Значение по умолчанию:Normal .

## Примеры

Показывает, как изменить цвет изображения с сохранением свойств параметров.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
// Установите свойство «ColorMode» на «Grayscale», чтобы отрисовать все изображения в документе в черно-белом цвете.
// При использовании этой настройки размер выходного документа может быть больше.
// Установите свойство «ColorMode» на «Normal», чтобы отображать все изображения в цвете.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Смотрите также

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
