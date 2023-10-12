---
title: MetafileRenderingOptions.EmulateRasterOperations
second_title: Referencia de API de Aspose.Words para .NET
description: MetafileRenderingOptions propiedad. Obtiene o establece un valor que determina si se deben emular o no las operaciones ráster.
type: docs
weight: 30
url: /es/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Obtiene o establece un valor que determina si se deben emular o no las operaciones ráster.

```csharp
public bool EmulateRasterOperations { get; set; }
```

### Observaciones

Se podrían utilizar operaciones ráster específicas en metarchivos. No se pueden representar directamente en gráficos vectoriales. La emulación de operaciones ráster requiere una rasterización parcial de los gráficos vectoriales resultantes, lo que puede afectar el rendimiento de procesamiento del metarchivo .

Cuando este valor se establece en`verdadero`, Aspose.Words emula las operaciones ráster. La salida resultante quizás esté parcialmente rasterizada y el rendimiento podría ser más lento.

Cuando este valor se establece en`FALSO`, Aspose.Words no emula las operaciones ráster. Cuando Aspose.Words encuentra una operación ráster en un metarchivo, recurre a representar el metarchivo en un mapa de bits utilizando el sistema operativo .

Esta opción se utiliza sólo cuando el metarchivo se representa como gráficos vectoriales.

El valor predeterminado es`verdadero`.

### Ejemplos

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

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../metafilerenderingoptions/)
* asamblea [Aspose.Words](../../../)


