---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Saving.SvgTextOutputMode, um die Textdarstellung im SVG-Format anzupassen und so die Präsentation und visuelle Attraktivität des Dokuments zu verbessern.
type: docs
weight: 6410
url: /de/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Ermöglicht die Angabe, wie Text in einem Dokument gerendert werden soll , wenn es im SVG-Format gespeichert wird.

```csharp
public enum SvgTextOutputMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG-Schriftarten werden zur Textdarstellung verwendet. Beachten Sie, dass nicht alle Browser SVG-Schriftarten unterstützen. |
| UseTargetMachineFonts | `1` | Zum Rendern von Text werden die auf dem Zielcomputer installierten Schriftarten verwendet. Beachten Sie: Wenn einige der im Dokument verwendeten Schriftarten auf dem Zielcomputer nicht verfügbar sind, kann das Dokument anders aussehen. |
| UsePlacedGlyphs | `2` | Der Text wird mithilfe von Kurven dargestellt. Beachten Sie, dass die Textauswahl bei Verwendung dieser Option nicht funktioniert. |

## Beispiele

Zeigt, wie die Eigenschaften von Bildern beim Konvertieren eines DOCX-Dokuments in SVG nachgeahmt werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurieren Sie das SvgSaveOptions-Objekt so, dass ohne Seitenränder oder auswählbaren Text gespeichert wird.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
