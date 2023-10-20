---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words für .NET
description: SvgSaveOptions FitToViewPort eigendom. Gibt an ob die AusgabeSVG den verfügbaren Ansichtsfensterbereich Browserfenster oder Container ausfüllen soll. Wenn auf gesetztWAHR Breite und Höhe der AusgabeSVG werden auf 100  gesetzt in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Gibt an, ob die Ausgabe-SVG den verfügbaren Ansichtsfensterbereich (Browserfenster oder Container) ausfüllen soll. Wenn auf gesetzt`WAHR` Breite und Höhe der Ausgabe-SVG werden auf 100 % gesetzt.

Der Standardwert ist`FALSCH`.

```csharp
public bool FitToViewPort { get; set; }
```

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

* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
