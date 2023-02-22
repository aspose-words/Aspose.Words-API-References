---
title: HtmlFixedSaveOptions.OptimizeOutput
second_title: Aspose.Words för .NET API Referens
description: HtmlFixedSaveOptions fast egendom. Flagga anger om det krävs för att optimera utdata. Om denna flagga ställs in redundanta kapslade dukar och tomma dukar tas bort sammanlänkas även grannglyfer med samma formatering. Obs Noggrannheten i innehållsvisningen kan påverkas den här egenskapen är satt till true. Standard är true.
type: docs
weight: 100
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Flagga anger om det krävs för att optimera utdata. Om denna flagga ställs in redundanta kapslade dukar och tomma dukar tas bort, sammanlänkas även grannglyfer med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas den här egenskapen är satt till true. Standard är true.

```csharp
public override bool OptimizeOutput { get; set; }
```

### Exempel

Visar hur man förenklar ett dokument när man sparar det i HTML genom att ta bort olika redundanta objekt.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// Storleken på den optimerade versionen av dokumentet är nästan en tredjedel av storleken på det ooptimerade dokumentet.
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* hopsättning [Aspose.Words](../../../)


