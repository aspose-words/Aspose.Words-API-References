---
title: FieldAddressBlock.IncludeCountryOrRegionName
linktitle: IncludeCountryOrRegionName
articleTitle: IncludeCountryOrRegionName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldAddressBlock IncludeCountryOrRegionName för att enkelt hantera inkludering av lands-/regionsnamn för förbättrad adressformatering.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldaddressblock/includecountryorregionname/
---
## FieldAddressBlock.IncludeCountryOrRegionName property

Hämtar eller anger om namnet på landet/regionen ska inkluderas.

```csharp
public string IncludeCountryOrRegionName { get; set; }
```

## Exempel

Visar hur man infogar ett ADRESSBLOCK-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Om du ställer in detta på "2" inkluderas alla länder och regioner,
// om det inte är den som anges i egenskapen ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// Som standard innehåller den här egenskapen språk-ID:t för det första tecknet i dokumentet.
// Vi kan ställa in en annan kultur för fältet för att formatera resultatet så här.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Se även

* class [FieldAddressBlock](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
