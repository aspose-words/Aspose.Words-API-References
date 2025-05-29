---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words ImlRenderingMode-Aufzählung für optimales InkML-Rendering. Verbessern Sie Ihre Dokumentausgabe mit präziser Tintenobjektvisualisierung!
type: docs
weight: 6000
url: /de/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Gibt an, wie InkML-Objekte (InkML) in feste Seitenformate gerendert werden.

```csharp
public enum ImlRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Fallback | `0` | Wenn eine Ersatzform für ein InkML-Objekt verfügbar ist, rendert Aspose.Words die Ersatzform anstelle von InkML. |
| InkML | `1` | Aspose.Words ignoriert die Fallback-Form des Ink-Objekts (InkML) und rendert InkML selbst. Dies ist der Standardmodus. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
