---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Füllfarbe“, um die Vordergrundfarbe Ihres Designs einfach mit einem Farbobjekt anzupassen und so die visuelle Attraktivität Ihres Projekts zu steigern.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Ruft ein Color-Objekt ab oder legt es fest, das die Vordergrundfarbe für die Füllung darstellt.

```csharp
public Color Color { get; set; }
```

## Bemerkungen

Diese Eigenschaft bewahrt die Alpha-Komponente desColor , im Gegensatz zu den[`ForeColor`](../forecolor/) Eigenschaft, die es auf eine vollständig undurchsichtige Farbe zurücksetzt.

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
