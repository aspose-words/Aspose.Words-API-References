---
title: Enum SvgTextOutputMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.SvgTextOutputMode opsomming. Ermöglicht die Angabe wie Text in einem Dokument gerendert werden soll beim Speichern im SVGFormat.
type: docs
weight: 5610
url: /de/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Ermöglicht die Angabe, wie Text in einem Dokument gerendert werden soll beim Speichern im SVG-Format.

```csharp
public enum SvgTextOutputMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG-Schriftarten werden zum Rendern von Text verwendet. Beachten Sie, dass nicht alle Browser SVG-Schriftarten unterstützen. |
| UseTargetMachineFonts | `1` | Auf dem Zielcomputer installierte Schriftarten werden zum Rendern von Text verwendet. Hinweis: Wenn einige der im Dokument verwendeten Schriftarten auf dem Zielcomputer nicht verfügbar sind, kann das Dokument anders aussehen. |
| UsePlacedGlyphs | `2` | Text wird mithilfe von Kurven gerendert. Beachten Sie, dass die Textauswahl nicht funktioniert, wenn Sie diese Option verwenden. |

### Beispiele

Zeigt, wie die Eigenschaften von Bildern beim Konvertieren eines .docx-Dokuments in .svg nachgeahmt werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurieren Sie das SVGSaveOptions-Objekt zum Speichern ohne Seitenränder oder auswählbaren Text.
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


