---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words för .NET
description: Upptäck typsnittsnamnÖvrigt. Anpassa enkelt typsnitt för teckenkoderna 128–255, vilket förbättrar din texts stil och läsbarhet. Förhöj din design idag!
type: docs
weight: 270
url: /sv/net/aspose.words/font/nameother/
---
## Font.NameOther property

Returnerar eller anger teckensnittet som används för tecken med teckenkoder från 128 till 255.

```csharp
public string NameOther { get; set; }
```

## Exempel

Visar hur Microsoft Word kan kombinera två olika teckensnitt i en omgång.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Antag en körning som vi använder byggaren för att infoga när vi använder denna typsnittskonfiguration
// innehåller tecken inom ASCII-tecknens intervall. I så fall,
// den kommer att visa de tecken som använder det här teckensnittet.
builder.Font.NameAscii = "Calibri";

// Om inget annat teckensnitt anges kommer verktyget även att använda detta teckensnitt på alla tecken som infogas.
Assert.AreEqual("Calibri", builder.Font.Name);

// Ange ett teckensnitt som ska användas för alla tecken utanför ASCII-området.
// Helst bör detta typsnitt ha en glyf för varje obligatorisk icke-ASCII-teckenkod.
builder.Font.NameOther = "Courier New";

// Infoga en sekvens med ett ord som består av ASCII-tecken och ett ord med alla tecken utanför det intervallet.
// Varje tecken visas med något av teckensnitten, beroende på.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Se även

* property [Name](../name/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
