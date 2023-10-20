---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words für .NET
description: SvgSaveOptions TextOutputMode eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt wie Text in SVG gerendert werden soll in C#.
type: docs
weight: 90
url: /de/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie Text in SVG gerendert werden soll.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Bemerkungen

Verwenden Sie diese Eigenschaft, um den Modus abzurufen oder festzulegen, wie Text in einem Dokument beim Speichern im SVG-Format gerendert werden soll .

Der Standardwert istUseTargetMachineFonts.

## Beispiele

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
