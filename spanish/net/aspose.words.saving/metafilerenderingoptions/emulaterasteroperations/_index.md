---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words para .NET
description: Descubra la propiedad MetafileRenderingOptions EmulateRasterOperations para controlar la emulación de operaciones ráster y mejorar sus capacidades de renderizado de manera efectiva.
type: docs
weight: 30
url: /es/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Obtiene o establece un valor que determina si las operaciones ráster deben emularse o no.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Observaciones

Se pueden usar operaciones raster específicas en metarchivos. No se pueden renderizar directamente en gráficos vectoriales. Emular operaciones raster requiere una rasterización parcial de los gráficos vectoriales resultantes, lo que puede afectar el rendimiento de renderizado de los metarchivos.

Cuando este valor se establece en`verdadero`Aspose.Words emula las operaciones rasterizadas. La salida resultante may está parcialmente rasterizada y el rendimiento podría ser más lento.

Cuando este valor se establece en`FALSO`Aspose.Words no emula las operaciones raster. Cuando Aspose.Words encuentra una operación raster en un metarchivo, recurre a la renderización del metarchivo en un mapa de bits mediante el sistema operativo .

Esta opción se utiliza sólo cuando el metarchivo se representa como gráficos vectoriales.

El valor predeterminado es`verdadero`.

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

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
