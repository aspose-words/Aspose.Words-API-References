---
title: FieldAddressBlock.LanguageId
linktitle: LanguageId
articleTitle: LanguageId
second_title: .NET için Aspose.Words
description: FieldAddressBlock LanguageId özelliğiyle adres biçimlendirmesini zahmetsizce yönetin. Sorunsuz yerelleştirme için dil kimliğini ayarlayın veya alın.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldaddressblock/languageid/
---
## FieldAddressBlock.LanguageId property

Adresi biçimlendirmek için kullanılan dil kimliğini alır veya ayarlar.

```csharp
public string LanguageId { get; set; }
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
