---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words für .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPage eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob das Rendern der Metadatei die Anzeige der Metadatei entsprechend der Größe auf page oder die Anzeige der Metadatei in ihrer Standardgröße emuliert in C#.
type: docs
weight: 40
url: /de/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob das Rendern der Metadatei die Anzeige der Metadatei entsprechend der Größe auf page oder die Anzeige der Metadatei in ihrer Standardgröße emuliert.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Bemerkungen

Wenn Metadateien in MS Word angezeigt werden, werden einige Grafiken möglicherweise entsprechend der tatsächlichen Metadateigröße in Pixeln skaliert. Das heißt, selbst das Zoomen kann die Anzeige der Metadatei beeinträchtigen.

Wenn dieser Wert auf eingestellt ist`WAHR` Aspose.Words emuliert das Rendern entsprechend der Metadateigröße auf der Seite. Die Größe in Pixel wird aus der Metadateigröße auf der Seite und der angegebenen Größe berechnet[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Wenn dieser Wert auf eingestellt ist`FALSCH`, Aspose.Words emuliert das Rendern von Metadateien auf ihre Standardgröße in Pixeln.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist`WAHR`.

## Beispiele

Zeigt, wie die Metadatei entsprechend der Größe auf der Seite angezeigt wird.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setze die Eigenschaft „EmulateRenderingToSizeOnPage“ auf „true“
// um das Rendern entsprechend der Metadateigröße auf der Seite zu emulieren.
// Setze die Eigenschaft „EmulateRenderingToSizeOnPage“ auf „false“
// um das Rendern von Metadateien auf ihre Standardgröße in Pixeln zu emulieren.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Siehe auch

* class [MetafileRenderingOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
