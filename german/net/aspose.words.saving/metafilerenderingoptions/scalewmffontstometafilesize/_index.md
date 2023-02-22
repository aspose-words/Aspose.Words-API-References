---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Aspose.Words für .NET-API-Referenz
description: MetafileRenderingOptions eigendom. Ruft einen Wert ab oder legt einen Wert fest der bestimmt ob Schriftarten in der WMFMetadatei entsprechend der Metadateigröße auf der Seite skaliert werden oder nicht.
type: docs
weight: 50
url: /de/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Schriftarten in der WMF-Metadatei entsprechend der Metadateigröße auf der Seite skaliert werden oder nicht.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### Bemerkungen

Wenn WMF-Metadateien in MS Word angezeigt werden, können Schriftarten gemäß der tatsächlichen Größe der Metadatei auf der Seite skaliert werden.

Wenn dieser Wert auf eingestellt ist`Stimmt`, Aspose.Words emuliert die Schriftskalierung entsprechend der Metadateigröße auf der Seite.

Wenn dieser Wert auf eingestellt ist`FALSCH`, Aspose.Words zeigt die Schriftarten an, während die Metadatei auf ihre Standardgröße gerendert wird.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist`Stimmt`.

### Beispiele

Zeigt, wie WMF-Schriftarten entsprechend der Metadateigröße auf der Seite skaliert werden.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft "ScaleWmfFontsToMetafileSize" auf "true", um Schriftarten zu skalieren
// die Text in WMF-Bildern entsprechend der Größe der Metadatei auf der Seite formatieren.
// Setzen Sie die Eigenschaft "ScaleWmfFontsToMetafileSize" auf "false".
// Standardmaßstab dieser Schriftarten beibehalten.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### Siehe auch

* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../metafilerenderingoptions/)
* Montage [Aspose.Words](../../../)


