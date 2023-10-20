---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words für .NET
description: MetafileRenderingOptions EmulateRasterOperations eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob die Rasteroperationen emuliert werden sollen oder nicht in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob die Rasteroperationen emuliert werden sollen oder nicht.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Bemerkungen

In Metadateien könnten bestimmte Rasteroperationen verwendet werden. Sie können nicht direkt in Vektorgrafiken gerendert werden. Das Emulieren von Rasteroperationen erfordert eine teilweise Rasterung der resultierenden Vektorgrafiken, was sich auf die Renderleistung der Metadatei auswirken kann.

Wenn dieser Wert auf eingestellt ist`WAHR`, Aspose.Words emuliert die Rasteroperationen. Die resultierende Ausgabe ist möglicherweise teilweise gerastert und die Leistung ist möglicherweise langsamer.

Wenn dieser Wert auf eingestellt ist`FALSCH`, Aspose.Words emuliert die Rasteroperationen nicht. Wenn Aspose.Words auf einen Rastervorgang in einer Metadatei stößt, greift es auf das Rendern der Metadatei in eine Bitmap mithilfe des -Betriebssystems zurück.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist`WAHR`.

## Beispiele

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

* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
