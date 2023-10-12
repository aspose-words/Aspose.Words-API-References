---
title: TxtSaveOptionsBase.ForcePageBreaks
second_title: Aspose.Words för .NET API Referens
description: TxtSaveOptionsBase fast egendom. Tillåter att ange om sidbrytningarna ska bevaras under export.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Tillåter att ange om sidbrytningarna ska bevaras under export.

Standardvärdet är`falsk`.

```csharp
public bool ForcePageBreaks { get; set; }
```

### Anmärkningar

Egenskapen påverkar endast sidbrytningar som infogas uttryckligen i ett dokument. Det är inte relaterat till sidbrytningar som MS Word automatiskt infogar i slutet av varje sida.

### Exempel

Visar hur man anger om sidbrytningar ska bevaras vid export av ett dokument till klartext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"
// metod för att ändra hur vi sparar dokumentet till klartext.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Aspose.Words "Document"-objekt har sidbrytningar, precis som Microsoft Word-dokument.
// Spara format som ".txt" är en sammanhängande text utan sidbrytningar.
// Ställ in egenskapen "ForcePageBreaks" på "true" för att bevara alla sidbrytningar i form av '\f'-tecken.
// Ställ in egenskapen "ForcePageBreaks" på "false" för att ignorera alla sidbrytningar.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Om vi laddar ett dokument i vanlig text med sidbrytningar,
// "Dokument"-objektet kommer att använda dem för att dela upp brödtexten i sidor.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Se även

* class [TxtSaveOptionsBase](../)
* namnutrymme [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* hopsättning [Aspose.Words](../../../)


