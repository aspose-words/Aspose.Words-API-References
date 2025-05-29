---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words för .NET
description: Optimera dokumenthanteringen med SaveOptions UpdateLastPrintedProperty. Kontrollera LastPrinted-uppdateringar för effektiv sparning och förbättrat arbetsflöde.
type: docs
weight: 180
url: /sv/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan den sparas.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Exempel

Visar hur man uppdaterar egenskapen "Senast utskriven" i ett dokument när det sparas.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// Denna flagga avgör om det senast utskrivna datumet, vilket är en inbyggd egenskap, uppdateras.
// Om så är fallet, då datumet för dokumentets senaste sparningsåtgärd
// med detta SaveOptions-objekt skickat som en parameter används det som utskriftsdatum.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// I Microsoft Word 2003 kan den här egenskapen hittas via Arkiv -> Egenskaper -> Statistik -> Utskrivet.
// Det kan också visas i dokumentets brödtext genom att använda ett PRINTDATE-fält.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Öppna det sparade dokumentet och verifiera sedan egenskapens värde.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
