---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
second_title: Aspose.Words für .NET-API-Referenz
description: MetafileRenderingOptions eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt wie EMF DualMetadateien gerendert werden sollen.
type: docs
weight: 20
url: /de/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

### Bemerkungen

EMF+ Dual-Metadateien enthalten sowohl EMF+- als auch EMF-Teile. MS Word und GDI+ rendern immer EMF+ part. Aspose.Words unterstützt derzeit nicht alle EMF+-Datensätze vollständig und in einigen Fällen sieht das Rendering-Ergebnis des EMF-Teils besser aus als das Rendering-Ergebnis des EMF+-Teils.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Wenn die Metadatei in eine Bitmap gerendert wird, wird immer der EMF+-Teil verwendet.

Der Standardwert istEmfPlusWithFallback.

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

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../metafilerenderingoptions/)
* Montage [Aspose.Words](../../../)


