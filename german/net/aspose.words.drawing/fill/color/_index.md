---
title: Fill.Color
second_title: Aspose.Words für .NET-API-Referenz
description: Fill eigendom. Ruft ein ColorObjekt ab oder legt dieses fest das die Vordergrundfarbe für die Füllung darstellt.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Ruft ein Color-Objekt ab oder legt dieses fest, das die Vordergrundfarbe für die Füllung darstellt.

```csharp
public Color Color { get; set; }
```

### Bemerkungen

Diese Eigenschaft bewahrt die Alpha-Komponente vonColor , im Gegensatz zum[`ForeColor`](../forecolor/)Eigenschaft, die es auf eine vollständig undurchsichtige Farbe zurücksetzt.

### Beispiele

Zeigt, wie eine der Füllungen wieder in eine Vollfüllung umgewandelt wird.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Fill-Objekt für Schriftart des ersten Laufs abrufen.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Fülleigenschaften der Schriftart prüfen.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Ändere den Typ der Füllung in „Fest“ mit einheitlicher grüner Farbe.
fill.Solid(Color.Green);
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../fill/)
* Montage [Aspose.Words](../../../)


