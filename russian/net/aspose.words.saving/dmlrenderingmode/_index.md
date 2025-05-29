---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words для .NET
description: Узнайте, как Aspose.Words.Saving.DmlRenderingMode улучшает визуализацию фигур DrawingML для высококачественных фиксированных форматов страниц. Оптимизируйте визуальные эффекты ваших документов!
type: docs
weight: 5670
url: /ru/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

Указывает, как фигуры DrawingML отображаются в фиксированных форматах страниц.

```csharp
public enum DmlRenderingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Fallback | `0` | Если для DrawingML доступна резервная фигура, Aspose.Words отображает резервную фигуру вместо DrawingML. |
| DrawingML | `1` | Aspose.Words игнорирует резервную форму DrawingML и отображает сам DrawingML. Это режим по умолчанию. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
