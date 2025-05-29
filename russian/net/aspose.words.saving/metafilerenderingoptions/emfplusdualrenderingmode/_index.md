---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words для .NET
description: Узнайте, как свойство EmfPlusDualRenderingMode улучшает рендеринг метафайла EMF Dual. Оптимизируйте свою графику с помощью гибких параметров рендеринга уже сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Возвращает или задает значение, определяющее, как следует отображать метафайлы EMF+ Dual.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## Примечания

Метафайлы EMF+ Dual содержат как части EMF+, так и EMF. MS Word и GDI+ всегда отображают часть EMF+. Aspose.Words в настоящее время не полностью поддерживает все записи EMF+, и в некоторых случаях результат отображения части EMF выглядит лучше, чем результат отображения части EMF+.

Эта опция используется только тогда, когда метафайл визуализируется как векторная графика. Когда метафайл визуализируется в битмап, всегда используется часть EMF+.

Значение по умолчанию:EmfPlusWithFallback.

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

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
