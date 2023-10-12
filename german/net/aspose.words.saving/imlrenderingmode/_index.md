---
title: Enum ImlRenderingMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.ImlRenderingMode opsomming. Gibt an wie InkObjekte InkML in feste Seitenformate gerendert werden.
type: docs
weight: 5250
url: /de/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Gibt an, wie Ink-Objekte (InkML) in feste Seitenformate gerendert werden.

```csharp
public enum ImlRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Fallback | `0` | Wenn eine Fallback-Form für ein Ink-Objekt (InkML) verfügbar ist, rendert Aspose.Words eine Fallback-Form anstelle von InkML. |
| InkML | `1` | Aspose.Words ignoriert die Fallback-Form des Ink-Objekts (InkML) und rendert InkML selbst. Dies ist der Standardmodus. |

### Beispiele

Zeigt, wie ein Ink-Objekt gerendert wird.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// „ImlRenderingMode.InkML“ festlegen, ignoriert die Fallback-Form des Ink-Objekts (InkML) und rendert InkML selbst.
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


