---
title: Enum MetafileRenderingMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.MetafileRenderingMode перечисление. Указывает как Aspose.Words должен отображать метафайлы WMF и EMF.
type: docs
weight: 5290
url: /ru/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

Указывает, как Aspose.Words должен отображать метафайлы WMF и EMF.

```csharp
public enum MetafileRenderingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words пытается визуализировать метафайл как векторную графику. Если Aspose.Words не может правильно преобразовать некоторые из записей метафайла в векторную графику, тогда Aspose.Words преобразует этот метафайл в растровое изображение. |
| Vector | `1` | Aspose.Words отображает метафайл как векторную графику. |
| Bitmap | `2` | Aspose.Words вызывает GDI+ для преобразования метафайла в растровое изображение, а затем сохраняет растровое изображение в выходной документ. |

### Примеры

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


