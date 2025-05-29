---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.ColorMode для оптимизированной цветопередачи. Улучшите визуальную привлекательность вашего документа с помощью точных настроек цвета.
type: docs
weight: 5600
url: /ru/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Указывает, как отображаются цвета.

```csharp
public enum ColorMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Рендеринг с немодифицированными цветами. |
| Grayscale | `1` | Рендеринг с цветами в диапазоне оттенков серого от белого до черного. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
