---
title: MetafileRenderingOptions.RenderingMode
linktitle: RenderingMode
articleTitle: RenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die RenderingMode-Eigenschaft von MetafileRenderingOptions, um zu steuern, wie Metadateibilder gerendert werden, und so die Qualität und Leistung Ihrer Grafiken zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Metadateibilder gerendert werden sollen.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

## Bemerkungen

Der Standardwert hängt vom Speicherformat ab. Für Bilder ist erBitmap . Für andere Formate ist esVectorWithFallback.

## Beispiele

Zeigt einen Fallback für die Bitmap-Wiedergabe und eine Änderung der Art der Warnungen zu nicht unterstützten Metadateidatensätzen an.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Setzen Sie die Eigenschaft "EmulateRasterOperations" auf "false", um auf Bitmap zurückzugreifen, wenn
    // Es wird auf eine Metadatei gestoßen, die Rasteroperationen erfordert, um sie im Ausgabe-PDF darzustellen.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Setzen Sie die Eigenschaft „RenderingMode“ auf „VectorWithFallback“, um zu versuchen, jede Metadatei mithilfe von Vektorgrafiken zu rendern.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie diese Methode das Dokument in .PDF konvertiert und die Konfiguration anwendet
    // in unserem MetafileRenderingOptions-Objekt zum Speichervorgang.
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
/// Druckt und sammelt Warnungen bezüglich Formatierungsverlust, die beim Speichern eines Dokuments auftreten.
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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
