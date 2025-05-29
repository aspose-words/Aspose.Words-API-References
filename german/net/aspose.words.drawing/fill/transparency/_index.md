---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words für .NET
description: Passen Sie die Fülltransparenz von 0,0 (undurchsichtig) bis 1,0 (transparent) an, um individuelle visuelle Effekte in Ihren Designs zu erzielen. Verbessern Sie noch heute die Ästhetik Ihres Projekts!
type: docs
weight: 200
url: /de/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

Ruft den Transparenzgrad der angegebenen Füllung als Wert zwischen 0,0 (undurchsichtig) und 1,0 (transparent) ab oder legt ihn fest.

```csharp
public double Transparency { get; set; }
```

## Bemerkungen

Diese Eigenschaft ist das Gegenteil von Eigentum[`Opacity`](../opacity/).

## Beispiele

Zeigt, wie Sie beliebige Füllungen wieder in Vollfüllungen umwandeln.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Füllobjekt für die Schriftart des ersten Laufs abrufen.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Fülleigenschaften der Schriftart prüfen.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Ändern Sie den Füllungstyp in „Einfarbig“ mit einheitlicher grüner Farbe.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
