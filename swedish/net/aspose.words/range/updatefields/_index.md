---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med metoden Range UpdateFields, som uppdaterar fältvärden snabbt och effektivt för förbättrad noggrannhet.
type: docs
weight: 130
url: /sv/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Uppdaterar värdena för dokumentfält i detta intervall.

```csharp
public void UpdateFields()
```

## Anmärkningar

När du öppnar, ändrar och sedan sparar ett dokument uppdaterar inte Aspose.Words fält automatiskt, utan behåller dem intakta. Därför bör du vanligtvis anropa den här metoden innan du sparar om du har ändrat dokumentet programmatiskt och vill se till att rätt (beräknade) fältvärden visas i det sparade dokumentet.

Det finns inget behov av att uppdatera fält efter att en dokumentkoppling har genomförts eftersom en dokumentkoppling är en typ av fältuppdatering och automatiskt uppdaterar alla fält i dokumentet.

Den här metoden uppdaterar inte alla fälttyper. En detaljerad lista över fälttyper som stöds finns i Programmer Guide.

Den här metoden uppdaterar inte fält som är relaterade till sidlayoutalgoritmerna (t.ex. PAGE, PAGES, PAGEREF). De sidlayoutrelaterade fälten uppdateras när du renderar ett dokument eller anropar[`UpdatePageLayout`](../../document/updatepagelayout/).

För att uppdatera fält i hela dokumentet, använd[`UpdateFields`](../../document/updatefields/).

## Exempel

Visar hur man uppdaterar alla fält i ett intervall.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Ovanstående DOCPROPERTY-fält visar värdet för den här inbyggda dokumentegenskapen.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Om vi uppdaterar värdet för en dokumentegenskap måste vi uppdatera alla DOCPROPERTY-fält för att visa det.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// Uppdatera alla fält som ligger inom intervallet för den första sektionen.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Se även

* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
