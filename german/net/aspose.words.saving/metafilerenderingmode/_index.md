---
title: MetafileRenderingMode Enum
linktitle: MetafileRenderingMode
articleTitle: MetafileRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Aspose.Words.Saving.MetafileRenderingMode das Rendern von WMF- und EMF-Metadateien für optimale Dokumentqualität und Leistung verbessert.
type: docs
weight: 6070
url: /de/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

Gibt an, wie Aspose.Words WMF- und EMF-Metadateien rendern soll.

```csharp
public enum MetafileRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words versucht, eine Metadatei als Vektorgrafik darzustellen. Wenn Aspose.Words einige der Datensätze der Metadatei nicht korrekt als Vektorgrafik darstellen kann, rendert Aspose.Words diese Metadatei in eine Bitmap. |
| Vector | `1` | Aspose.Words rendert eine Metadatei als Vektorgrafik. |
| Bitmap | `2` | Aspose.Words ruft GDI+ auf, um eine Metadatei in eine Bitmap zu rendern und speichert die Bitmap dann im Ausgabedokument. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
