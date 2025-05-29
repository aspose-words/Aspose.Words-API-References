---
title: FieldAddressBlock.ExcludedCountryOrRegionName
linktitle: ExcludedCountryOrRegionName
articleTitle: ExcludedCountryOrRegionName
second_title: .NET için Aspose.Words
description: FieldAddressBlock ExcludedCountryOrRegionName özelliğiyle hariç tutulan ülkeleri/bölgeleri zahmetsizce yönetin. Adres işlemenizi bugün optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldaddressblock/excludedcountryorregionname/
---
## FieldAddressBlock.ExcludedCountryOrRegionName property

Hariç tutulan ülke/bölge adını alır veya ayarlar.

```csharp
public string ExcludedCountryOrRegionName { get; set; }
```

## Örnekler

ADDRESSBLOCK alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Bunu "2" olarak ayarlamak tüm ülkeleri ve bölgeleri kapsayacaktır.
// ExcludedCountryOrRegionName özelliğinde belirtilen olmadığı sürece.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// Varsayılan olarak bu özellik, belgenin ilk karakterinin dil kimliğini içerecektir.
// Sonucu bu şekilde biçimlendirmek için alan için farklı bir kültür ayarlayabiliriz.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Ayrıca bakınız

* class [FieldAddressBlock](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
