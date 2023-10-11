---
title: FixedPageSaveOptions.OptimizeOutput
second_title: Aspose.Words för .NET API Referens
description: FixedPageSaveOptions fast egendom. Flagga indikerar om det krävs för att optimera utdata. Om denna flagga ställs in redundanta kapslade dukar och tomma dukar tas bort sammanlänkas även grannglyfer med samma formatering. Obs Noggrannheten i innehållsvisningen kan påverkas den här egenskapen är inställd påSann . Standard ärfalsk .
type: docs
weight: 50
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Flagga indikerar om det krävs för att optimera utdata. Om denna flagga ställs in redundanta kapslade dukar och tomma dukar tas bort, sammanlänkas även grannglyfer med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas den här egenskapen är inställd på`Sann` . Standard är`falsk` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

### Exempel

Visar hur man optimerar dokumentobjekt samtidigt som man sparar till xps.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Skapa ett "XpsSaveOptions"-objekt för att skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

// Ställ in egenskapen "OptimizeOutput" på "true" för att vidta åtgärder som att ta bort kapslade eller tomma dukar
// och sammanlänkning av angränsande körningar med identisk formatering för att optimera utdatadokumentets innehåll.
// Detta kan påverka utseendet på dokumentet.
// Ställ in egenskapen "OptimizeOutput" till "false" för att spara dokumentet normalt.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Se även

* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* hopsättning [Aspose.Words](../../../)


