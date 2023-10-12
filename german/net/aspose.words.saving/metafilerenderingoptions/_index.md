---
title: Class MetafileRenderingOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.MetafileRenderingOptions klas. Ermöglicht die Angabe zusätzlicher MetadateiRenderingOptionen.
type: docs
weight: 5300
url: /de/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Ermöglicht die Angabe zusätzlicher Metadatei-Rendering-Optionen.

Um mehr zu erfahren, besuchen Sie die[Umgang mit Windows-Metadateien](https://docs.aspose.com/words/net/handling-windows-metafiles/) Dokumentationsartikel.

```csharp
public class MetafileRenderingOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob die Rasteroperationen emuliert werden sollen oder nicht. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob das Rendern der Metadatei die Anzeige der Metadatei entsprechend der Größe auf page oder die Anzeige der Metadatei in ihrer Standardgröße emuliert. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Ruft die Auflösung in Pixel pro Zoll für die Emulation des Metadatei-Renderings auf die Größe auf der Seite ab oder legt diese fest. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie Metadateibilder gerendert werden sollen. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie WMF-Metadateien mit eingebetteten EMF-Metadateien gerendert werden sollen. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


