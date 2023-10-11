---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
second_title: Справочник по API Aspose.Words для .NET
description: MetafileRenderingOptions свойство. Получает или задает значение определяющее как должны отображаться метафайлы WMF со встроенными метафайлами EMF.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Получает или задает значение, определяющее, как должны отображаться метафайлы WMF со встроенными метафайлами EMF.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

### Примечания

Метафайлы WMF могут содержать встроенные данные EMF. MS Word в большинстве случаев использует встроенные данные EMF. GDI+ всегда использует данные WMF.

Когда это значение установлено на`истинный`, Aspose.Words использует встроенные данные EMF при рендеринге.

Когда это значение установлено на`ЛОЖЬ`, Aspose.Words использует данные WMF при рендеринге.

Этот параметр используется только в том случае, если метафайл отображается как векторная графика. Когда метафайл преобразуется в растровое изображение, всегда используются данные WMF.

Значение по умолчанию:`истинный`.

### Примеры

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

* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../metafilerenderingoptions/)
* сборка [Aspose.Words](../../../)


