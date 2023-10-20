---
title: MetafileRenderingOptions.RenderingMode
linktitle: RenderingMode
articleTitle: RenderingMode
second_title: Aspose.Words для .NET
description: MetafileRenderingOptions RenderingMode свойство. Получает или задает значение определяющее способ отображения изображений метафайлов на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

Получает или задает значение, определяющее способ отображения изображений метафайлов.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

## Примечания

Значение по умолчанию зависит от формата сохранения. Для изображений этоBitmap . Для других форматов этоVectorWithFallback.

## Примеры

Показывает добавлен запасной вариант рендеринга растровых изображений и изменение типа предупреждений о неподдерживаемых записях метафайлов.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Установите для свойства «EmulateRasterOperations» значение «false», чтобы вернуться к растровому изображению при
    // он обнаруживает метафайл, для рендеринга которого в выходном PDF-файле потребуются растровые операции.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Установите для свойства «RenderingMode» значение «VectorWithFallback», чтобы попытаться отобразить каждый метафайл с использованием векторной графики.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
    // чтобы изменить способ преобразования этого метода в .PDF и применения конфигурации
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
/// Печатает и собирает предупреждения, связанные с потерей форматирования, возникающие при сохранении документа.
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
