---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft EmfPlusDualRenderingMode das Rendering von EMF-Dual-Metadateien verbessert. Optimieren Sie Ihre Grafiken noch heute mit flexiblen Rendering-Optionen!
type: docs
weight: 20
url: /de/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## Bemerkungen

EMF+ Dual-Metadateien enthalten sowohl EMF+- als auch EMF-Teile. MS Word und GDI+ rendern immer EMF+-Teile. Aspose.Words unterstützt derzeit nicht alle EMF+-Datensätze vollständig und in einigen Fällen sieht das Rendering-Ergebnis des EMF-Teils besser aus als das Rendering-Ergebnis des EMF+-Teils.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Beim Rendern der Metadatei in Bitmap wird immer der EMF+-Anteil verwendet.

Der Standardwert istEmfPlusWithFallback.

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

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
