---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words EMF Plus Dual Rendering Mode для оптимального рендеринга метафайла EMF Dual. Улучшите обработку документов с точностью!
type: docs
weight: 5730
url: /ru/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Указывает, как Aspose.Words должен отображать метафайлы EMF+ Dual.

```csharp
public enum EmfPlusDualRenderingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words пытается отобразить часть EMF+ метафайла EMF+ Dual. Если некоторые записи EMF+ не поддерживаются , то Aspose.Words отобразит часть EMF метафайла EMF+ Dual. |
| EmfPlus | `1` | Aspose.Words отображает EMF+ часть метафайла EMF+ Dual. |
| Emf | `2` | Aspose.Words отображает часть EMF метафайла EMF+ Dual. |

## Примеры

Показывает, как настроить параметры рендеринга, связанные с расширенными метафайлами Windows, при сохранении в формате PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите свойство "EmfPlusDualRenderingMode" на "EmfPlusDualRenderingMode.Emf"
// для визуализации только части EMF двойного метафайла EMF+.
// Установите свойство "EmfPlusDualRenderingMode" в "EmfPlusDualRenderingMode.EmfPlus" для
// для визуализации части EMF+ двойного метафайла EMF+.
// Установите свойство "EmfPlusDualRenderingMode" на "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// для отображения части EMF+ двойного метафайла EMF+, если поддерживаются все записи EMF+.
// В противном случае Aspose.Words отобразит часть EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Установите свойство "UseEmfEmbeddedToWmf" в значение "true" для отображения встроенных данных EMF
// для метафайлов, которые мы можем визуализировать как векторную графику.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
