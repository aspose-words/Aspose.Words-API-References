---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words för .NET
description: Förbättra dina dokumentutdata med FixedPageSaveOptions egenskap OptimizeOutput. Ta bort redundanser och förbättra formateringen för tydligare visning.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Flaggan anger om det är nödvändigt att optimera utdata. Om denna flagga är inställd tas redundanta kapslade arbetsytor och tomma arbetsytor bort, sammanfogas även angränsande tecken med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas om den här egenskapen är inställd på`sann` . Standard är`falsk` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Exempel

Visar hur man optimerar dokumentobjekt när man sparar till XPS.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Skapa ett "XpsSaveOptions"-objekt för att skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();
// Sätt egenskapen "OptimizeOutput" till "true" för att vidta åtgärder som att ta bort kapslade eller tomma arbetsytor
// och sammanfogar intilliggande körningar med identisk formatering för att optimera innehållet i utdatadokumentet.
// Detta kan påverka dokumentets utseende.
// Sätt egenskapen "OptimizeOutput" till "false" för att spara dokumentet normalt.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Se även

* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
