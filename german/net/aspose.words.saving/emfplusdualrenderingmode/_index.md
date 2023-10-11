---
title: Enum EmfPlusDualRenderingMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.EmfPlusDualRenderingMode opsomming. Gibt an wie Aspose.Words EMF DualMetadateien rendern soll.
type: docs
weight: 4980
url: /de/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Gibt an, wie Aspose.Words EMF+ Dual-Metadateien rendern soll.

```csharp
public enum EmfPlusDualRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words versucht, EMF+ als Teil der EMF+ Dual-Metadatei darzustellen. Wenn einige der EMF+-Datensätze nicht unterstützt werden , rendert Aspose.Words EMF als Teil der EMF+ Dual-Metadatei. |
| EmfPlus | `1` | Aspose.Words rendert EMF+ als Teil der EMF+ Dual-Metadatei. |
| Emf | `2` | Aspose.Words rendert EMF als Teil der EMF+ Dual-Metadatei. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


