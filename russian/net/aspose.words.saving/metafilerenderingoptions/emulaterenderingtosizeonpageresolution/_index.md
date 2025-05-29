---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution. Управляйте разрешением рендеринга метафайла для оптимального отображения страницы.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Возвращает или задает разрешение в пикселях на дюйм для эмуляции рендеринга метафайла до размера на странице.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Примечания

Эта опция используется только тогда, когда[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) установлен на`истинный`.

Значение по умолчанию — 96. Это разрешение экрана по умолчанию. То есть рендеринг метафайла будет эмулировать отображение метафайла в MS Word с коэффициентом масштабирования 100%.

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
