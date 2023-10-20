---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words для .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPage свойство. Получает или задает значение определяющее эмулирует ли отрисовка метафайла отображение метафайла в соответствии с размером на странице или отображение метафайла с размером по умолчанию на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Получает или задает значение, определяющее, эмулирует ли отрисовка метафайла отображение метафайла в соответствии с размером на странице или отображение метафайла с размером по умолчанию.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Примечания

Когда метафайлы отображаются в MS Word, некоторая графика может масштабироваться в соответствии с фактическим размером метафайла в пикселях. Т.е. даже масштабирование может повлиять на отображение метафайла.

Когда это значение установлено на`истинный` Aspose.Words эмулирует рендеринг в соответствии с размером метафайла на странице. Размер в пикселях рассчитывается на основе размера метафайла на странице и указанного[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Когда это значение установлено на`ЛОЖЬ`, Aspose.Words эмулирует рендеринг метафайла до размера по умолчанию в пикселях.

Этот параметр используется только в том случае, если метафайл отображается как векторная графика.

Значение по умолчанию:`истинный`.

## Примеры

Показывает, как отображать метафайл в зависимости от размера на странице.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства "EmulateRenderingToSizeOnPage" значение "true"
// для эмуляции рендеринга в соответствии с размером метафайла на странице.
// Установите для свойства «EmulateRenderingToSizeOnPage» значение «false»
// для эмуляции рендеринга метафайла до размера по умолчанию в пикселях.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Смотрите также

* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
