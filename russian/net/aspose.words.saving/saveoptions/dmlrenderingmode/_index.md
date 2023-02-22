---
title: SaveOptions.DmlRenderingMode
second_title: Справочник по API Aspose.Words для .NET
description: SaveOptions свойство. Получает или задает значение определяющее способ визуализации фигур DrawingML.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

Получает или задает значение, определяющее способ визуализации фигур DrawingML.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

### Примечания

Значение по умолчанию:Fallback .

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

### Примеры

Показывает, как визуализировать резервные фигуры при сохранении в PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства "DmlRenderingMode" значение "DmlRenderingMode.Fallback"
// для замены форм DML их резервными формами.
// Установите для свойства "DmlRenderingMode" значение "DmlRenderingMode.DrawingML"
// для рендеринга самих форм DML.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Показывает, как настроить качество рендеринга эффектов DrawingML в документе при его сохранении в формате PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства "DmlEffectsRenderingMode" значение "DmlEffectsRenderingMode.None", чтобы отменить все эффекты DrawingML.
// Установите для свойства "DmlEffectsRenderingMode" значение "DmlEffectsRenderingMode.Simplified"
// для визуализации упрощенной версии эффектов DrawingML.
// Установите для свойства "DmlEffectsRenderingMode" значение "DmlEffectsRenderingMode.Fine", чтобы
// визуализировать эффекты DrawingML с большей точностью, а также с большей стоимостью обработки.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Смотрите также

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../saveoptions/)
* сборка [Aspose.Words](../../../)


