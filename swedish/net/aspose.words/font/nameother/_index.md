---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words för .NET
description: Font NameOther fast egendom. Returnerar eller ställer in teckensnittet som används för tecken med teckenkoder från 128 till 255 i C#.
type: docs
weight: 270
url: /sv/net/aspose.words/font/nameother/
---
## Font.NameOther property

Returnerar eller ställer in teckensnittet som används för tecken med teckenkoder från 128 till 255.

```csharp
public string NameOther { get; set; }
```

## Exempel

Visar hur Microsoft Word kan kombinera två olika typsnitt i en körning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Antag en körning som vi använder byggaren för att infoga när vi använder den här teckensnittskonfigurationen
// innehåller tecken inom ASCII-teckens intervall. Isåfall,
// det kommer att visa dessa tecken med detta teckensnitt.
builder.Font.NameAscii = "Calibri";

// Utan något annat teckensnitt specificerat kommer byggaren också att tillämpa detta teckensnitt på alla tecken som den infogar.
Assert.AreEqual("Calibri", builder.Font.Name);

// Ange ett teckensnitt som ska användas för alla tecken utanför ASCII-intervallet.
// Helst bör detta teckensnitt ha en glyf för varje obligatorisk icke-ASCII-teckenkod.
builder.Font.NameOther = "Courier New";

// Infoga en körning med ett ord som består av ASCII-tecken och ett ord med alla tecken utanför det intervallet.
// Varje tecken kommer att visas med något av teckensnitten, beroende på.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Se även

* property [Name](../name/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
