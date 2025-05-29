---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die FitToViewPort-Eigenschaft von SvgSaveOptions Ihre SVG-Ausgabe optimiert, um jedes Browserfenster oder jeden Container perfekt auszufüllen und beeindruckende visuelle Darstellungen zu erzielen.
type: docs
weight: 30
url: /de/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Gibt an, ob das Ausgabe-SVG den verfügbaren Ansichtsbereich (Browserfenster oder Container) ausfüllen soll. Wenn auf`WAHR`Breite und Höhe des Ausgabe-SVG sind auf 100 % eingestellt.

Der Standardwert ist`FALSCH`.

```csharp
public bool FitToViewPort { get; set; }
```

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

* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
