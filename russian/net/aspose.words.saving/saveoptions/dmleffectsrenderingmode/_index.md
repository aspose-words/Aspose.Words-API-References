---
title: SaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words для .NET
description: SaveOptions DmlEffectsRenderingMode свойство. Получает или задает значение определяющее способ визуализации эффектов DrawingML на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

Получает или задает значение, определяющее способ визуализации эффектов DrawingML.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Примечания

Значение по умолчанию:Simplified .

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

## Примеры

Показывает, как настроить качество рендеринга эффектов DrawingML в документе при его сохранении в формате PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства «DmlEffectsRenderingMode» значение «DmlEffectsRenderingMode.None», чтобы отменить все эффекты DrawingML.
// Установите для свойства "DmlEffectsRenderingMode" значение "DmlEffectsRenderingMode.Simplified"
// для рендеринга упрощенной версии эффектов DrawingML.
// Установите для свойства "DmlEffectsRenderingMode" значение "DmlEffectsRenderingMode.Fine", чтобы
// визуализируем эффекты DrawingML с большей точностью, а также с большими затратами на обработку.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Смотрите также

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
