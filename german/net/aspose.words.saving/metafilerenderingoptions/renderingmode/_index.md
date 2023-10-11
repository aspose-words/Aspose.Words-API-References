---
title: MetafileRenderingOptions.RenderingMode
second_title: Aspose.Words für .NET-API-Referenz
description: MetafileRenderingOptions eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt wie Metadateibilder gerendert werden sollen.
type: docs
weight: 60
url: /de/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie Metadateibilder gerendert werden sollen.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

### Bemerkungen

Der Standardwert hängt vom Speicherformat ab. Für Bilder ist es soBitmap . Für andere Formate gilt diesVectorWithFallback.

### Beispiele

Zeigt einen Fallback für die Bitmap-Wiedergabe und eine Änderung der Art von Warnungen zu nicht unterstützten Metadateidatensätzen an.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Setzen Sie die Eigenschaft „EmulateRasterOperations“ auf „false“, um auf die Bitmap zurückzugreifen, wenn
    // es trifft auf eine Metadatei, die Rasteroperationen zum Rendern in der Ausgabe-PDF erfordert.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Setzen Sie die Eigenschaft „RenderingMode“ auf „VectorWithFallback“, um zu versuchen, jede Metadatei mithilfe von Vektorgrafiken zu rendern.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
    // um zu ändern, wie diese Methode das Dokument in .PDF konvertiert und die Konfiguration anwendet
    // in unserem MetafileRenderingOptions-Objekt für den Speichervorgang.
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
/// Druckt und sammelt Warnungen im Zusammenhang mit Formatierungsverlusten, die beim Speichern eines Dokuments auftreten.
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

### Siehe auch

* enum [MetafileRenderingMode](../../metafilerenderingmode/)
* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../metafilerenderingoptions/)
* Montage [Aspose.Words](../../../)


