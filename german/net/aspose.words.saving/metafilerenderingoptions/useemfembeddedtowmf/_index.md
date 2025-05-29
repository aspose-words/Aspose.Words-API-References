---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft UseEmfEmbeddedToWmf das Rendern von WMF-Metadateien optimiert und so die Leistung und Qualität Ihrer Grafikanwendungen verbessert.
type: docs
weight: 70
url: /de/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie WMF-Metadateien mit eingebetteten EMF-Metadateien gerendert werden sollen.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Bemerkungen

WMF-Metadateien können eingebettete EMF-Daten enthalten. MS Word verwendet in den meisten Fällen eingebettete EMF-Daten. GDI+ verwendet immer WMF-Daten.

Wenn dieser Wert auf`WAHR`, Aspose.Words verwendet beim Rendern eingebettete EMF-Daten.

Wenn dieser Wert auf`FALSCH`, Aspose.Words verwendet beim Rendern WMF-Daten.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Beim Rendern der Metadatei in Bitmap werden immer WMF-Daten verwendet.

Der Standardwert ist`WAHR`.

## Beispiele

Zeigt, wie Sie beim Speichern im PDF-Format erweiterte Windows-Metafile-bezogene Rendering-Optionen konfigurieren.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „EmfPlusDualRenderingMode“ auf „EmfPlusDualRenderingMode.Emf“
// um nur den EMF-Teil einer EMF+-Dual-Metadatei zu rendern.
// Setzen Sie die Eigenschaft "EmfPlusDualRenderingMode" auf "EmfPlusDualRenderingMode.EmfPlus" auf
// um den EMF+-Teil einer EMF+-Dual-Metadatei zu rendern.
// Setzen Sie die Eigenschaft „EmfPlusDualRenderingMode“ auf „EmfPlusDualRenderingMode.EmfPlusWithFallback“
// um den EMF+-Teil einer EMF+-Dual-Metadatei zu rendern, wenn alle EMF+-Datensätze unterstützt werden.
// Andernfalls rendert Aspose.Words den EMF-Teil.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Setzen Sie die Eigenschaft „UseEmfEmbeddedToWmf“ auf „true“, um eingebettete EMF-Daten zu rendern
// für Metadateien, die wir als Vektorgrafiken rendern können.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Siehe auch

* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
