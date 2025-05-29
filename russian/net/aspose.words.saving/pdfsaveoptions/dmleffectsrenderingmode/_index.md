---
title: PdfSaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions DmlEffectsRenderingMode для управления рендерингом эффектов DrawingML для повышения качества вывода PDF.
type: docs
weight: 100
url: /ru/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

Возвращает или задает значение, определяющее способ визуализации эффектов DrawingML.

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Примечания

Значение по умолчанию:Simplified .

Это свойство используется при экспорте документа в форматы с фиксированным размером страницы.

Если[`Compliance`](../compliance/) установлен наPdfA1a илиPdfA1b , свойство всегда возвращаетNone.

## Примеры

Показывает, как настроить качество рендеринга эффектов DrawingML в документе при его сохранении в формате PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "DmlEffectsRenderingMode" в "DmlEffectsRenderingMode.None", чтобы отменить все эффекты DrawingML.
// Установите свойство "DmlEffectsRenderingMode" на "DmlEffectsRenderingMode.Simplified"
// для визуализации упрощенной версии эффектов DrawingML.
// Установите свойство "DmlEffectsRenderingMode" на "DmlEffectsRenderingMode.Fine" для
// визуализировать эффекты DrawingML с большей точностью, но и с большими затратами на обработку.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Смотрите также

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
