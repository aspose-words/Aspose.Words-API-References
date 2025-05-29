---
title: Font.NameAscii
linktitle: NameAscii
articleTitle: NameAscii
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font NameAscii för att anpassa latinska textteckensnitt och förbättra din design med teckenkoder 0–127 för förbättrad läsbarhet.
type: docs
weight: 240
url: /sv/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

Returnerar eller anger teckensnittet som används för latinsk text (tecken med teckenkoder från 0 (noll) till 127).

```csharp
public string NameAscii { get; set; }
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
