---
title: MetafileRenderingOptions.RenderingMode
linktitle: RenderingMode
articleTitle: RenderingMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство RenderingMode MetafileRenderingOptions, чтобы управлять рендерингом изображений метафайлов, повышая качество графики и производительность.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

Возвращает или задает значение, определяющее, как должны отображаться изображения метафайлов.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

## Примечания

Значение по умолчанию зависит от формата сохранения. Для изображений этоBitmap . Для других форматов этоVectorWithFallback.

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

* enum [MetafileRenderingMode](../../metafilerenderingmode/)
* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
