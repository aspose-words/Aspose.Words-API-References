---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SaveOptions ImlRenderingMode-Eigenschaft die InkML-Objektdarstellung verbessert. Optimieren Sie Ihre Ink-Darstellung für bessere visuelle Ergebnisse!
type: docs
weight: 90
url: /de/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie InkML-Objekte gerendert werden.

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Bemerkungen

Der Standardwert istInkML .

Diese Eigenschaft wird verwendet, wenn das Dokument in feste Seitenformate exportiert wird.

## Beispiele

Zeigt, wie Ink-Objekte gerendert werden.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Set 'ImlRenderingMode.InkML' ignoriert die Fallback-Form des Ink-Objekts (InkML) und rendert InkML selbst.
// Wenn das Rendering-Ergebnis unbefriedigend ist,
// Bitte verwenden Sie „ImlRenderingMode.Fallback“, um ein ähnliches Ergebnis wie in früheren Versionen zu erhalten.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Siehe auch

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
