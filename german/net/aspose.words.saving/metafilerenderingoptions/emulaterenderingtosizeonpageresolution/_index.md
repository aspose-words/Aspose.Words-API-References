---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution“. Steuern Sie die Auflösung des Metafile-Renderings für eine optimale Seitenanzeige.
type: docs
weight: 50
url: /de/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Ruft die Auflösung in Pixeln pro Zoll für die Emulation der Metadateiwiedergabe auf die Größe auf der Seite ab oder legt sie fest.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Bemerkungen

Diese Option wird nur verwendet, wenn[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) ist eingestellt auf`WAHR`.

Der Standardwert ist 96. Dies ist die Standardanzeigeauflösung. Das heißt, die Metadatei-Darstellung emuliert die Anzeige von der Metadatei in MS Word mit einem Zoomfaktor von 100 %.

## Beispiele

Zeigt, wie die Metadatei entsprechend der Größe auf der Seite angezeigt wird.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „EmulateRenderingToSizeOnPage“ auf „true“
// um das Rendering entsprechend der Metadateigröße auf der Seite zu emulieren.
// Setzen Sie die Eigenschaft „EmulateRenderingToSizeOnPage“ auf „false“
// um die Metadateidarstellung auf ihre Standardgröße in Pixeln zu emulieren.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Siehe auch

* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
