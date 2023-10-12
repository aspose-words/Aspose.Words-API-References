---
title: Range.UpdateFields
second_title: Aspose.Words för .NET API Referens
description: Range metod. Uppdaterar värdena för dokumentfält i detta intervall.
type: docs
weight: 120
url: /sv/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Uppdaterar värdena för dokumentfält i detta intervall.

```csharp
public void UpdateFields()
```

### Anmärkningar

När du öppnar, ändrar och sedan sparar ett dokument uppdaterar Aspose.Words inte fält automatiskt, det behåller dem intakta. Därför skulle du vanligtvis vilja anropa den här metoden innan du sparar om du har modifierat document programmatiskt och vill försäkra dig om de korrekta (beräknade) fältvärdena visas i det sparade dokumentet.

Det finns inget behov av att uppdatera fält efter att ha kört en sammankoppling eftersom brevkoppling är ett slags fält update och uppdaterar automatiskt alla fält i dokumentet.

Denna metod uppdaterar inte alla fälttyper. För en detaljerad lista över fälttyper som stöds, se Programmers Guide.

Den här metoden uppdaterar inte fält som är relaterade till sidlayoutalgoritmerna (t.ex. PAGE, PAGES, PAGEREF). De sidlayoutrelaterade fälten uppdateras när du renderar ett dokument eller anropar[`UpdatePageLayout`](../../document/updatepagelayout/).

För att uppdatera fält i hela dokumentet använd[`UpdateFields`](../../document/updatefields/).

### Exempel

Visar hur du uppdaterar alla fält i ett intervall.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Ovanstående DOCPROPERTY-fält visar värdet för denna inbyggda dokumentegenskap.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Om vi uppdaterar värdet på en dokumentegenskap måste vi uppdatera alla DOCPROPERTY-fält för att visa den.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// Uppdatera alla fält som är inom intervallet för det första avsnittet.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Se även

* class [Range](../)
* namnutrymme [Aspose.Words](../../range/)
* hopsättning [Aspose.Words](../../../)


