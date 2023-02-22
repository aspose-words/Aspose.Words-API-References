---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
second_title: Справочник по API Aspose.Words для .NET
description: MetafileRenderingOptions свойство. Получает или задает значение определяющее способ отображения метафайлов WMF со встроенными метафайлами EMF.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Получает или задает значение, определяющее способ отображения метафайлов WMF со встроенными метафайлами EMF.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

### Примечания

Метафайлы WMF могут содержать встроенные данные EMF. MS Word в большинстве случаев использует встроенные данные EMF. GDI+ всегда использует данные WMF.

Когда это значение установлено на`истинный`, Aspose.Words использует встроенные данные EMF при рендеринге.

Когда это значение установлено на`ЛОЖЬ`, Aspose.Words использует данные WMF при рендеринге.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика. Когда метафайл преобразуется в растровое изображение, всегда используются данные WMF.

Значение по умолчанию`истинный`.

### Примеры

Показывает, как настроить параметры рендеринга, связанные с расширенным метафайлом Windows, при сохранении в PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства "EmfPlusDualRenderingMode" значение "EmfPlusDualRenderingMode.Emf"
// для рендеринга только части EMF двойного метафайла EMF+.
// Установите для свойства "EmfPlusDualRenderingMode" значение "EmfPlusDualRenderingMode.EmfPlus", чтобы
// для рендеринга части EMF+ двойного метафайла EMF+.
// Установите для свойства "EmfPlusDualRenderingMode" значение "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// для рендеринга части EMF+ двойного метафайла EMF+, если поддерживаются все записи EMF+.
// В противном случае Aspose.Words отобразит часть EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Установите для свойства «UseEmfEmbeddedToWmf» значение «true», чтобы визуализировать встроенные данные EMF
// для метафайлов, которые мы можем отображать как векторную графику.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Смотрите также

* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../metafilerenderingoptions/)
* сборка [Aspose.Words](../../../)


