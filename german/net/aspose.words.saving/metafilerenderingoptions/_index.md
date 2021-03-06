---
title: MetafileRenderingOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Ermöglicht die Angabe zusätzlicher Metadatei-Wiedergabeoptionen.
type: docs
weight: 5020
url: /de/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Ermöglicht die Angabe zusätzlicher Metadatei-Wiedergabeoptionen.

```csharp
public class MetafileRenderingOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die Rasteroperationen emuliert werden sollen oder nicht. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Metadateibilder gerendert werden sollen. |
| [ScaleWmfFontsToMetafileSize](../../aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Schriftarten in der WMF-Metadatei entsprechend der Metadateigröße auf der Seite skaliert werden oder nicht. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie WMF-Metadateien mit eingebetteten EMF-Metadateien gerendert werden sollen. |

### Beispiele

Shows hat einen Fallback zum Bitmap-Rendering hinzugefügt und die Art der Warnungen über nicht unterstützte Metadatei-Datensätze geändert.

```csharp
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Setzen Sie die Eigenschaft "EmulateRasterOperations" auf "false", um auf Bitmap zurückzugreifen, wenn
    // Es trifft auf eine Metadatei, die Rasteroperationen zum Rendern in der Ausgabe-PDF erfordert.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Setzen Sie die Eigenschaft "RenderingMode" auf "VectorWithFallback", um zu versuchen, jede Metadatei mit Vektorgrafiken zu rendern.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie diese Methode das Dokument in .PDF konvertiert und die Konfiguration anwendet
    // in unserem MetafileRenderingOptions-Objekt für den Speichervorgang.
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
/// Druckt und sammelt Formatierungsverlust-bezogene Warnungen, die beim Speichern eines Dokuments auftreten.
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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
