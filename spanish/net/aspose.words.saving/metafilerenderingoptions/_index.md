---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Saving.MetafileRenderingOptions para un mejor control y personalización de la representación de metarchivos en sus documentos. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 6080
url: /es/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Permite especificar opciones adicionales de representación de metarchivos.

Para obtener más información, visite el[Manejo de metarchivos de Windows](https://docs.aspose.com/words/net/handling-windows-metafiles/) Artículo de documentación.

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
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Obtiene o establece un valor que determina si las operaciones ráster deben emularse o no. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Obtiene o establece un valor que determina si la representación del metarchivo emula la visualización del metarchivo según el tamaño de la página o la visualización del metarchivo en su tamaño predeterminado. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Obtiene o establece la resolución en píxeles por pulgada para la emulación de la representación del metarchivo al tamaño de la página. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo deben representarse las imágenes de metarchivo. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Obtiene o establece un valor que determina cómo se deben representar los metarchivos WMF con metarchivos EMF integrados. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Obtiene o establece un valor que determina si se debe utilizar o no GDI+ para la emulación de operaciones ráster. |

## Ejemplos

Se agregó una alternativa a la representación de mapas de bits y se cambió el tipo de advertencias sobre registros de metarchivos no compatibles.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Establezca la propiedad "EmulateRasterOperations" en "false" para volver al mapa de bits cuando
    // encuentra un metarchivo, que requerirá operaciones rasterizadas para renderizarse en el PDF de salida.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Establezca la propiedad "RenderingMode" en "VectorWithFallback" para intentar renderizar cada metarchivo utilizando gráficos vectoriales.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
    // para modificar cómo ese método convierte el documento a .PDF y aplica la configuración
    // en nuestro objeto MetafileRenderingOptions para la operación de guardado.
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
/// Imprime y recopila advertencias relacionadas con la pérdida de formato que se producen al guardar un documento.
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
