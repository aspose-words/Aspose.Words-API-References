---
title: "Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion metodu"
linktitle: "get_FormatAddressOnCountryOrRegion"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion metodu. Alıcının ülke/bölgesine göre adresi POST*CODE (Universal Postal Union 2006) tanımına göre biçimlendirip biçimlendirmeyeceğini C++'ta alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fields/fieldaddressblock/get_formataddressoncountryorregion/
---
## FieldAddressBlock::get_FormatAddressOnCountryOrRegion method


Alıcı ülke/bölgesine göre adresi POST*CODE (Evrensel Posta Birliği 2006) tanımına göre biçimlendirip biçimlendirmeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion()
```


## Örnekler



ADDRESSBLOCK alanının nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// Bunu "2" olarak ayarlamak tüm ülkeleri ve bölgeleri dahil eder,
// istisna olarak ExcludedCountryOrRegionName özelliğinde belirtilen ülke/bölge hariç tutulur.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// Varsayılan olarak, bu özellik belgenin ilk karakterinin dil kimliğini içerir.
// Alan için sonucu farklı bir kültürle biçimlendirmek üzere şöyle bir ayar yapabiliriz.
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## Ayrıca Bakınız

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
