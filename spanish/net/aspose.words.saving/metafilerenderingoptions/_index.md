---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.Saving.MetafileRenderingOptions clase. Permite especificar opciones adicionales de representación de metarchivos en C#.
type: docs
weight: 5300
url: /es/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Permite especificar opciones adicionales de representación de metarchivos.

Para obtener más información, visite el[Manejo de metarchivos de Windows](https://docs.aspose.com/words/net/handling-windows-metafiles/) artículo de documentación.

```csharp
public class MetafileRenderingOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se deben representar los metarchivos duales EMF+. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Obtiene o establece un valor que determina si se deben emular o no las operaciones ráster. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Obtiene o establece un valor que determina si la representación del metarchivo emula la visualización del metarchivo según el tamaño en la página o la visualización del metarchivo en su tamaño predeterminado. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Obtiene o establece la resolución en píxeles por pulgada para la emulación de la representación de metarchivos al tamaño de la página. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se deben representar las imágenes de metarchivo. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Obtiene o establece un valor que determina cómo se deben representar los metarchivos WMF con metarchivos EMF incrustados. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Obtiene o establece un valor que determina si se utiliza o no GDI+ para la emulación de operaciones ráster. |

## Ejemplos

Los programas agregaron un respaldo a la representación de mapas de bits y cambiaron el tipo de advertencias sobre registros de metarchivos no compatibles.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Establece la propiedad "EmulateRasterOperations" en "false" para volver al mapa de bits cuando
    // encuentra un metarchivo que requerirá operaciones de trama para representar el PDF de salida.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Establece la propiedad "RenderingMode" en "VectorWithFallback" para intentar renderizar cada metarchivo usando gráficos vectoriales.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
    // para modificar cómo ese método convierte el documento a .PDF y aplica la configuración
    // en nuestro objeto MetafileRenderingOptions para la operación de guardar.
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
/// Imprime y recopila advertencias relacionadas con la pérdida de formato que ocurren al guardar un documento.
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

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
