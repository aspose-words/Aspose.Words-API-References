---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words для .NET
description: Узнайте, как свойство EmulateRenderingToSizeOnPage улучшает рендеринг метафайлов, гарантируя точные размеры отображения для оптимальных визуальных результатов.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Возвращает или задает значение, определяющее, эмулирует ли рендеринг метафайла отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Примечания

При отображении метафайлов в MS Word некоторые графические изображения могут масштабироваться в соответствии с фактическим размером метафайла в пикселях. Т.е. даже масштабирование может повлиять на отображение метафайла.

Когда это значение установлено на`истинный` Aspose.Words эмулирует рендеринг в соответствии с размером метафайла на странице. Размер в пикселях рассчитывается из размера метафайла на странице и указанного[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Когда это значение установлено на`ЛОЖЬ`Aspose.Words эмулирует рендеринг метафайла до размера по умолчанию в пикселях.

Эта опция используется только в том случае, если метафайл отображается как векторная графика.

Значение по умолчанию:`истинный`.

## Примеры

Показывает, как отображать метафайл в зависимости от размера на странице.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите свойство "EmulateRenderingToSizeOnPage" в значение "true"
// для эмуляции рендеринга в соответствии с размером метафайла на странице.
// Установите свойство "EmulateRenderingToSizeOnPage" в значение "false"
// для эмуляции рендеринга метафайла до размера по умолчанию в пикселях.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Смотрите также

* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
