---
title: Fill.Solid
second_title: Aspose.Words für .NET-API-Referenz
description: Fill methode. Setzt die Füllung auf eine einheitliche Farbe.
type: docs
weight: 260
url: /de/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Setzt die Füllung auf eine einheitliche Farbe.

```csharp
public void Solid()
```

### Bemerkungen

Verwenden Sie diese Methode, um beliebige Füllungen wieder in eine Vollfüllung umzuwandeln.

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../fill/)
* Montage [Aspose.Words](../../../)

---

## Solid(Color) {#solid_1}

Setzt die Füllung auf eine bestimmte einheitliche Farbe.

```csharp
public void Solid(Color color)
```

### Bemerkungen

Verwenden Sie diese Methode, um beliebige Füllungen wieder in eine Vollfüllung umzuwandeln.

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


