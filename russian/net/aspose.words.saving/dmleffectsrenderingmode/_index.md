---
title: Enum DmlEffectsRenderingMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.DmlEffectsRenderingMode перечисление. Указывает как эффекты DrawingML отображаются в фиксированных форматах страниц.
type: docs
weight: 4910
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
| Fine | `2` | Эффекты DrawingML визуализируются в тонком режиме, который включает расширенную обработку. В этом режиме рендеринг эффектов дает лучшие результаты, но с более высокими затратами производительности, чемSimplified режим. |

### Примеры

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


