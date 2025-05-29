---
title: FixedPageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words para .NET
description: Descubra la propiedad MetafileRenderingOptions de FixedPageSaveOptions para personalizar y mejorar la representación de su metarchivo para obtener resultados óptimos.
type: docs
weight: 30
url: /es/net/aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/
---
## FixedPageSaveOptions.MetafileRenderingOptions property

Permite especificar opciones de representación de metarchivos.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; set; }
```

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

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [FixedPageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
