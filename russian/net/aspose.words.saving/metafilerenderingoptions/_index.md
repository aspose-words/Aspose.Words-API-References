---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Saving.MetafileRenderingOptions для улучшенного управления рендерингом метафайлов и настройки в ваших документах. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 6080
url: /ru/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Позволяет указать дополнительные параметры рендеринга метафайла.

Чтобы узнать больше, посетите[Обработка метафайлов Windows](https://docs.aspose.com/words/net/handling-windows-metafiles/) документальная статья.

```csharp
public class MetafileRenderingOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее, как следует отображать метафайлы EMF+ Dual. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Возвращает или задает значение, определяющее, следует ли эмулировать растровые операции. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Возвращает или задает значение, определяющее, эмулирует ли рендеринг метафайла отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Возвращает или задает разрешение в пикселях на дюйм для эмуляции рендеринга метафайла до размера на странице. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Возвращает или задает значение, определяющее, как должны отображаться изображения метафайлов. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Возвращает или задает значение, определяющее, как должны отображаться метафайлы WMF со встроенными метафайлами EMF. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать GDI+ для эмуляции растровых операций. |

## Примеры

В шоу добавлена возможность отката к растровому рендерингу и изменен тип предупреждений о неподдерживаемых записях метафайлов.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Установите свойство "EmulateRasterOperations" в значение "false", чтобы вернуться к растровому изображению, когда
    // он обнаруживает метафайл, для рендеринга которого в выходном PDF-файле потребуются растровые операции.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Установите свойство «RenderingMode» на «VectorWithFallback», чтобы попытаться визуализировать каждый метафайл с использованием векторной графики.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
    // чтобы изменить способ преобразования этим методом документа в .PDF и применения конфигурации
    // в нашем объекте MetafileRenderingOptions для операции сохранения.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is not supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Печатает и собирает предупреждения, связанные с потерей форматирования, которые возникают при сохранении документа.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
