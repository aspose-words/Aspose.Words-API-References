---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words DmlEffectsRenderingMode для оптимизированного рендеринга эффектов DrawingML в фиксированных форматах страниц. Улучшите качество вашего документа!
type: docs
weight: 5660
url: /ru/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

Указывает, как эффекты DrawingML отображаются в фиксированных форматах страниц.

```csharp
public enum DmlEffectsRenderingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Simplified | `0` | Упрощен рендеринг эффектов DrawingML. |
| None | `1` | Эффекты DrawingML не отображаются. |
| Fine | `2` | Эффекты DrawingML визуализируются в точном режиме, который включает расширенную обработку. В этом режиме визуализация эффектов дает лучшие результаты, но с более высокими затратами производительности, чемSimplified режим. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
