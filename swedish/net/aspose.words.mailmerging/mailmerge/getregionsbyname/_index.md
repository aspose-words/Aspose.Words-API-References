---
title: MailMerge.GetRegionsByName
second_title: Aspose.Words för .NET API Referens
description: MailMerge metod. Returnerar en samling kopplingsregioner med det angivna namnet.
type: docs
weight: 240
url: /sv/net/aspose.words.mailmerging/mailmerge/getregionsbyname/
---
## MailMerge.GetRegionsByName method

Returnerar en samling kopplingsregioner med det angivna namnet.

```csharp
public IList<MailMergeRegionInfo> GetRegionsByName(string regionName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| regionName | String | Regionnamn (skiftlägeskänsligt). |

### Returvärde

Listan över regioner.

### Exempel

Visar hur man skapar, listar och läser kopplingsregioner.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "TableStart" och "TableEnd"-taggar, som går inuti MERGEFIELDs,
// betecknar strängarna som anger början och slut på kopplingsregioner.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Använd dessa taggar för att starta och avsluta en kopplingsregion med namnet "MailMergeRegion1",
// som kommer att innehålla MERGEFIELDs för två kolumner.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Vi kan hålla reda på sammanslagna regioner och deras kolumner genom att titta på dessa samlingar.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Infoga en region med samma namn i den befintliga regionen, vilket gör den till en förälder.
// Nu kommer ett "Kolumn2"-fält att finnas i en ny region.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Om vi slår upp namnet på dubbletter av regioner med metoden "GetRegionsByName",
// det kommer att returnera alla sådana regioner i en samling.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Kontrollera att den andra regionen nu har en överordnad region.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Se även

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)


