---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die TextOutputMode-Eigenschaft von SvgSaveOptions, die die Textdarstellung in SVG für verbesserte visuelle Qualität und individuelle Anpassung steuert. Optimieren Sie Ihre Grafiken noch heute!
type: docs
weight: 120
url: /de/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie Text in SVG gerendert werden soll.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Bemerkungen

Verwenden Sie diese Eigenschaft, um den Modus abzurufen oder festzulegen, wie Text in einem Dokument beim Speichern im SVG-Format gerendert werden soll .

Der Standardwert istUseTargetMachineFonts.

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
