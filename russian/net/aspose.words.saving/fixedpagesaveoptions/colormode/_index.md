---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words для .NET
description: FixedPageSaveOptions ColorMode свойство. Получает или задает значение определяющее способ отображения цветов на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Получает или задает значение, определяющее способ отображения цветов.

```csharp
public ColorMode ColorMode { get; set; }
```

## Примечания

Значение по умолчанию:Normal .

## Примеры

Показывает, как изменить цвет изображения с сохранением свойства параметров.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
// Установите для свойства «ColorMode» значение «Оттенки серого», чтобы отобразить все изображения из документа в черно-белом режиме.
// Размер выходного документа может быть больше с этой настройкой.
// Установите для свойства ColorMode значение «Normal», чтобы отобразить все изображения в цвете.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Смотрите также

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
