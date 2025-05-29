---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SaveOptions DmlRenderingMode улучшает визуализацию фигур DrawingML. Оптимизируйте визуальные элементы документа без усилий!
type: docs
weight: 70
url: /ru/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

Возвращает или задает значение, определяющее способ визуализации фигур DrawingML.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## Примечания

Значение по умолчанию:Fallback .

Это свойство используется при экспорте документа в форматы с фиксированным размером страницы.

## Примеры

Показывает, как отображать резервные фигуры при сохранении в PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "DmlRenderingMode" на "DmlRenderingMode.Fallback"
// для замены фигур DML их резервными фигурами.
// Установите свойство "DmlRenderingMode" на "DmlRenderingMode.DrawingML"
// для визуализации самих фигур DML.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

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

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
