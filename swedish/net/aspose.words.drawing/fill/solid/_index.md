---
title: Fill.Solid
second_title: Aspose.Words för .NET API Referens
description: Fill metod. Ställer in fyllningen till en enhetlig färg.
type: docs
weight: 200
url: /sv/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Ställer in fyllningen till en enhetlig färg.

```csharp
public void Solid()
```

### Anmärkningar

Använd den här metoden för att konvertera någon av fyllningarna tillbaka till solid fill.

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../fill/)
* hopsättning [Aspose.Words](../../../)

---

## Solid(Color) {#solid_1}

Ställer in fyllningen till en specificerad enhetlig färg.

```csharp
public void Solid(Color color)
```

### Anmärkningar

Använd den här metoden för att konvertera någon av fyllningarna tillbaka till solid fill.

### Exempel

Visar hur man konverterar någon av fyllningarna tillbaka till fast fyllning.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Hämta Fill-objekt för teckensnitt för den första körningen.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Kontrollera fyllningsegenskaperna för teckensnittet.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Ändra typ av fyllning till Solid med enhetlig grön färg.
fill.Solid(Color.Green);
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../fill/)
* hopsättning [Aspose.Words](../../../)


