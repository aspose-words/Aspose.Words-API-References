---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words för .NET
description: Styr sidbrytningar med TxtSaveOptionsBases ForcePageBreaks-egenskap. Säkerställ sömlös export och underhåll dokumentformatering utan ansträngning.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Gör det möjligt att ange om sidbrytningarna ska bevaras under export.

Standardvärdet är`falsk`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Anmärkningar

Egenskapen påverkar endast sidbrytningar som infogas explicit i ett dokument. Den är inte relaterad till sidbrytningar som MS Word automatiskt infogar i slutet av varje sida.

## Exempel

Visar hur man anger om sidbrytningar ska behållas när man exporterar ett dokument till klartext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-funktion.
// metod för att ändra hur vi sparar dokumentet till klartext.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Aspose.Words "Dokument"-objekt har sidbrytningar, precis som Microsoft Word-dokument.
// Sparformat som ".txt" är en sammanhängande text utan sidbrytningar.
// Sätt egenskapen "ForcePageBreaks" till "true" för att bevara alla sidbrytningar i form av '\f'-tecken.
// Sätt egenskapen "ForcePageBreaks" till "false" för att ignorera alla sidbrytningar.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Om vi laddar ett klartextdokument med sidbrytningar,
// objektet "Dokument" kommer att använda dem för att dela upp brödtexten i sidor.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Se även

* class [TxtSaveOptionsBase](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
