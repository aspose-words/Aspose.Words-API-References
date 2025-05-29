---
title: MailMerge.RegionEndTag
linktitle: RegionEndTag
articleTitle: RegionEndTag
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RegionEndTag för MailMerge för att effektivt hantera dina kopplingsområden. Förenkla dokumentautomation med sömlös taggintegration.
type: docs
weight: 90
url: /sv/net/aspose.words.mailmerging/mailmerge/regionendtag/
---
## MailMerge.RegionEndTag property

Hämtar eller ställer in en sluttagg för ett regionsavsnitt för dokumentkoppling.

```csharp
public string RegionEndTag { get; set; }
```

## Exempel

Visar hur man skapar, listar och läser områden för dokumentkoppling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "TableStart"- och "TableEnd"-taggarna, som placeras inuti MERGEFIELDS,
// betecknar strängarna som anger början och slut för områden för koppling av dokument.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Använd dessa taggar för att starta och avsluta en region för dokumentkoppling med namnet "MailMergeRegion1",
// som kommer att innehålla MERGEFIELDS för två kolumner.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Vi kan hålla reda på sammanslagningsregioner och deras kolumner genom att titta på dessa samlingar.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Infoga en region med samma namn inuti den befintliga regionen, vilket gör den till en förälder.
// Nu kommer fältet "Kolumn2" att finnas inuti en ny region.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Om vi söker upp namnet på duplicerade regioner med hjälp av metoden "GetRegionsByName",
// den kommer att returnera alla sådana regioner i en samling.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Kontrollera att den andra regionen nu har en överordnad region.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
