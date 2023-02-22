---
title: FieldAddressBlock.NameAndAddressFormat
second_title: Aspose.Words for .NET API Referansı
description: FieldAddressBlock mülk. Ad ve adres biçimini alır veya ayarlar.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldaddressblock/nameandaddressformat/
---
## FieldAddressBlock.NameAndAddressFormat property

Ad ve adres biçimini alır veya ayarlar.

```csharp
public string NameAndAddressFormat { get; set; }
```

### Örnekler

ADRESBLOCK alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Bunu "2" olarak ayarlamak tüm ülkeleri ve bölgeleri içerecektir,
// ExcludedCountryOrRegionName özelliğinde belirtilen değilse.
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
* ad alanı [Aspose.Words.Fields](../../fieldaddressblock/)
* toplantı [Aspose.Words](../../../)


