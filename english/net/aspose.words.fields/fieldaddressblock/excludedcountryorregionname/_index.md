---
title: FieldAddressBlock.ExcludedCountryOrRegionName
linktitle: ExcludedCountryOrRegionName
articleTitle: ExcludedCountryOrRegionName
second_title: Aspose.Words for .NET
description: Manage excluded countries/regions effortlessly with the FieldAddressBlock ExcludedCountryOrRegionName property. Optimize your address handling today!
type: docs
weight: 20
url: /net/aspose.words.fields/fieldaddressblock/excludedcountryorregionname/
---
## FieldAddressBlock.ExcludedCountryOrRegionName property

Gets or sets the excluded country/region name.

```csharp
public string ExcludedCountryOrRegionName { get; set; }
```

## Examples

Shows how to insert an ADDRESSBLOCK field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.That(field.GetFieldCode(), Is.EqualTo(" ADDRESSBLOCK "));

// Setting this to "2" will include all countries and regions,
// unless it is the one specified in the ExcludedCountryOrRegionName property.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// By default, this property will contain the language ID of the first character of the document.
// We can set a different culture for the field to format the result with like this.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.That(field.GetFieldCode(), Is.EqualTo(" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033"));
```

### See Also

* class [FieldAddressBlock](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
