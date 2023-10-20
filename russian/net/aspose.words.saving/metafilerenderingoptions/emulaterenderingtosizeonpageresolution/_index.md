---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words для .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution свойство. Получает или задает разрешение в пикселях на дюйм для эмуляции рендеринга метафайла до размера на странице на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Получает или задает разрешение в пикселях на дюйм для эмуляции рендеринга метафайла до размера на странице.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Примечания

Эта опция используется только тогда, когда[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) установлено на`истинный`.

Значение по умолчанию — 96. Это разрешение экрана по умолчанию. Т.е. рендеринг метафайла будет эмулировать отображение метафайла в MS Word со 100% коэффициентом масштабирования.

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
