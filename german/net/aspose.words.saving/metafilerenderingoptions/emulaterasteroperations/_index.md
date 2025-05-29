---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „EmulateRasterOperations“ von MetafileRenderingOptions, um die Emulation von Rasteroperationen zu steuern und so Ihre Rendering-Funktionen effektiv zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die Rasteroperationen emuliert werden sollen oder nicht.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Bemerkungen

Bestimmte Rasteroperationen können in Metadateien verwendet werden. Sie können nicht direkt in Vektorgrafiken gerendert werden. Die Emulation von Rasteroperationen erfordert eine teilweise Rasterung der resultierenden Vektorgrafiken, was die Renderleistung der Metadatei beeinträchtigen kann.

Wenn dieser Wert auf`WAHR`Aspose.Words emuliert die Rasteroperationen. Die resultierende Ausgabe ist möglicherweise teilweise gerastert und die Leistung kann beeinträchtigt sein.

Wenn dieser Wert auf`FALSCH`Aspose.Words emuliert die Rasteroperationen nicht. Wenn Aspose.Words auf eine Rasteroperation in einer Metadatei stößt, wird die Metadatei mithilfe des Betriebssystems in eine Bitmap gerendert.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist`WAHR`.

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

* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
