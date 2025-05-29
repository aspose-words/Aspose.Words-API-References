---
title: Fill.FillType
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die FillType-Eigenschaft effektiv festlegen und Ihr Design mit anpassbaren Fülloptionen für eine bessere visuelle Wirkung verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.drawing/fill/filltype/
---
## Fill.FillType property

Ruft einen Fülltyp ab.

```csharp
public FillType FillType { get; }
```

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

* enum [FillType](../../filltype/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
