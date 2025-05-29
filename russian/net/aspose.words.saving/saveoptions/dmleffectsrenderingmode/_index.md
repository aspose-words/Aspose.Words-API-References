---
title: SaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SaveOptions DmlEffectsRenderingMode оптимизирует рендеринг эффектов DrawingML для повышения качества и производительности документа.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

Возвращает или задает значение, определяющее способ визуализации эффектов DrawingML.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Примечания

Значение по умолчанию:Simplified .

Это свойство используется при экспорте документа в форматы с фиксированным размером страницы.

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
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
