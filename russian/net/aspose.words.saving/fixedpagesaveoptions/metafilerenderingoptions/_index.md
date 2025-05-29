---
title: FixedPageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MetafileRenderingOptions класса FixedPageSaveOptions, чтобы настроить и улучшить рендеринг метафайлов для достижения оптимальных результатов.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/
---
## FixedPageSaveOptions.MetafileRenderingOptions property

Позволяет указать параметры рендеринга метафайла.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; set; }
```

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

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
