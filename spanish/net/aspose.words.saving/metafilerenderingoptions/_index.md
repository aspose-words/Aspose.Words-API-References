---
title: Class MetafileRenderingOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.MetafileRenderingOptions clase. Permite especificar opciones adicionales de representación de metarchivos.
type: docs
weight: 5020
url: /es/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Permite especificar opciones adicionales de representación de metarchivos.

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
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se deben representar los metarchivos EMF+ Dual. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Obtiene o establece un valor que determina si se deben emular o no las operaciones de ráster. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se deben representar las imágenes de metarchivo. |
| [ScaleWmfFontsToMetafileSize](../../aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/) { get; set; } | Obtiene o establece un valor que determina si escalar o no las fuentes en el metarchivo WMF según el tamaño del metarchivo en la página. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Obtiene o establece un valor que determina cómo se deben representar los metarchivos WMF con metarchivos EMF incrustados. |

### Ejemplos

Los espectáculos agregaron una alternativa a la representación de mapas de bits y cambiaron el tipo de advertencias sobre registros de metarchivos no admitidos.

```csharp
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Establezca la propiedad "EmulateRasterOperations" en "false" para volver al mapa de bits cuando
    // encuentra un metarchivo, que requerirá operaciones de trama para representar en el PDF de salida.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Establezca la propiedad "RenderingMode" en "VectorWithFallback" para intentar representar cada metarchivo utilizando gráficos vectoriales.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
    // para modificar cómo ese método convierte el documento a .PDF y aplica la configuración
    // en nuestro objeto MetafileRenderingOptions para la operación de guardado.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is partly supported.",
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


