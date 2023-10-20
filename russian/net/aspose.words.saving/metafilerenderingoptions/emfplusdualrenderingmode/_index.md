---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words для .NET
description: MetafileRenderingOptions EmfPlusDualRenderingMode свойство. Получает или задает значение определяющее способ отображения метафайлов EMF Dual на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Получает или задает значение, определяющее способ отображения метафайлов EMF+ Dual.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## Примечания

Метафайлы EMF+ Dual содержат как части EMF+, так и EMF. MS Word и GDI+ всегда отображают часть EMF+. Aspose.Words в настоящее время не полностью поддерживает все записи EMF+, и в некоторых случаях результат рендеринга части EMF выглядит лучше, чем результат рендеринга части EMF+.

Этот параметр используется только в том случае, если метафайл отображается как векторная графика. Когда метафайл преобразуется в растровое изображение, всегда используется часть EMF+.

Значение по умолчанию:EmfPlusWithFallback.

## Примеры

Показывает, как настроить параметры рендеринга, связанные с расширенными метафайлами Windows, при сохранении в PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства «EmfPlusDualRenderingMode» значение «EmfPlusDualRenderingMode.Emf»
// для визуализации только части EMF двойного метафайла EMF+.
// Установите для свойства «EmfPlusDualRenderingMode» значение «EmfPlusDualRenderingMode.EmfPlus», чтобы
// для визуализации части EMF+ двойного метафайла EMF+.
// Установите для свойства «EmfPlusDualRenderingMode» значение «EmfPlusDualRenderingMode.EmfPlusWithFallback»
// для визуализации части EMF+ двойного метафайла EMF+, если все записи EMF+ поддерживаются.
// В противном случае Aspose.Words отобразит часть EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Установите для свойства UseEmfEmbeddedToWmf значение «true», чтобы отображать встроенные данные EMF.
// для метафайлов, которые мы можем визуализировать как векторную графику.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Смотрите также

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
