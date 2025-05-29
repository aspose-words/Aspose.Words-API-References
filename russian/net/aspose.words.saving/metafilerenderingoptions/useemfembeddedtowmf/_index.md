---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words для .NET
description: Узнайте, как свойство UseEmfEmbeddedToWmf оптимизирует рендеринг метафайла WMF, повышая производительность и качество ваших графических приложений.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Возвращает или задает значение, определяющее, как должны отображаться метафайлы WMF со встроенными метафайлами EMF.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Примечания

Метафайлы WMF могут содержать встроенные данные EMF. MS Word в большинстве случаев использует встроенные данные EMF. GDI+ всегда использует данные WMF.

Когда это значение установлено на`истинный`Aspose.Words использует встроенные данные EMF при рендеринге.

Когда это значение установлено на`ЛОЖЬ`, Aspose.Words использует данные WMF при рендеринге.

Эта опция используется только тогда, когда метафайл визуализируется как векторная графика. Когда метафайл визуализируется в битмап, всегда используются данные WMF.

Значение по умолчанию:`истинный`.

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

* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
