---
title: FieldAddressBlock.FormatAddressOnCountryOrRegion
linktitle: FormatAddressOnCountryOrRegion
articleTitle: FormatAddressOnCountryOrRegion
second_title: Aspose.Words för .NET
description: Optimera adressformateringen med egenskapen FieldAddressBlock FormatAddressOnCountryOrRegion, vilket säkerställer att globala poststandarder för korrekt leverans följs.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/
---
## FieldAddressBlock.FormatAddressOnCountryOrRegion property

Hämtar eller anger om adressen ska formateras enligt mottagarens land/region enligt definitionen i POST*CODE (Universal Postal Union 2006).

```csharp
public bool FormatAddressOnCountryOrRegion { get; set; }
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
