---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „EmulateRenderingToSizeOnPage“ die Metadateiwiedergabe verbessert und genaue Anzeigegrößen für optimale visuelle Ergebnisse gewährleistet.
type: docs
weight: 40
url: /de/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob beim Rendern der Metadatei die Anzeige der Metadatei entsprechend der Größe auf Seite oder die Anzeige der Metadatei in ihrer Standardgröße emuliert wird.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Bemerkungen

Wenn Metadateien in MS Word angezeigt werden, werden einige Grafiken möglicherweise entsprechend der tatsächlichen Metadateigröße in Pixeln skaliert. Das heißt, selbst das Zoomen kann die Anzeige der Metadatei beeinträchtigen.

Wenn dieser Wert auf`WAHR` Aspose.Words emuliert das Rendering entsprechend der Metadateigröße auf der Seite. Die Größe in Pixeln wird aus der Metadateigröße auf der Seite und der angegebenen berechnet[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Wenn dieser Wert auf`FALSCH`, Aspose.Words emuliert die Metadatei-Wiedergabe auf ihre Standardgröße in Pixeln.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist`WAHR`.

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
