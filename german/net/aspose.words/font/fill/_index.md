---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Schriftfüllung“, um das Erscheinungsbild Ihres Textes mit anpassbarer Füllformatierung für ein elegantes, professionelles Aussehen zu verbessern.
type: docs
weight: 130
url: /de/net/aspose.words/font/fill/
---
## Font.Fill property

Ruft die Füllformatierung für die[`Font`](../) .

```csharp
public Fill Fill { get; }
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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
