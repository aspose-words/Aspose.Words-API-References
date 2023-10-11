---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
second_title: Aspose.Words für .NET-API-Referenz
description: MetafileRenderingOptions eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt wie WMFMetadateien mit eingebetteten EMFMetadateien gerendert werden sollen.
type: docs
weight: 70
url: /de/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie WMF-Metadateien mit eingebetteten EMF-Metadateien gerendert werden sollen.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

### Bemerkungen

WMF-Metadateien könnten eingebettete EMF-Daten enthalten. MS Word verwendet in den meisten Fällen eingebettete EMF-Daten. GDI+ verwendet immer WMF-Daten.

Wenn dieser Wert auf eingestellt ist`WAHR`, Aspose.Words verwendet beim Rendern eingebettete EMF-Daten.

Wenn dieser Wert auf eingestellt ist`FALSCH`, Aspose.Words verwendet beim Rendern WMF-Daten.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Wenn die Metadatei in eine Bitmap gerendert wird, werden immer WMF-Daten verwendet.

Der Standardwert ist`WAHR`.

### Beispiele

Zeigt, wie erweiterte Windows-Metadatei-bezogene Rendering-Optionen beim Speichern als PDF konfiguriert werden.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setze die Eigenschaft „EmfPlusDualRenderingMode“ auf „EmfPlusDualRenderingMode.Emf“
// um nur den EMF-Teil einer EMF+-Dual-Metadatei zu rendern.
// Setzen Sie die Eigenschaft „EmfPlusDualRenderingMode“ auf „EmfPlusDualRenderingMode.EmfPlus“.
// um den EMF+-Teil einer EMF+-Dual-Metadatei zu rendern.
// Setze die Eigenschaft „EmfPlusDualRenderingMode“ auf „EmfPlusDualRenderingMode.EmfPlusWithFallback“
// um den EMF+-Teil einer EMF+-Dual-Metadatei zu rendern, wenn alle EMF+-Datensätze unterstützt werden.
// Andernfalls rendert Aspose.Words den EMF-Teil.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Setzen Sie die Eigenschaft „UseEmfEmbeddedToWmf“ auf „true“, um eingebettete EMF-Daten darzustellen
// für Metadateien, die wir als Vektorgrafiken rendern können.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Siehe auch

* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../metafilerenderingoptions/)
* Montage [Aspose.Words](../../../)


