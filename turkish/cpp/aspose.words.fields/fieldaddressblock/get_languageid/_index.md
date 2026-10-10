---
title: "Aspose::Words::Fields::FieldAddressBlock::get_LanguageId yöntemi"
linktitle: "get_LanguageId"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldAddressBlock::get_LanguageId yöntemi. C++'ta adresi biçimlendirmek için kullanılan dil kimliğini alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fields/fieldaddressblock/get_languageid/
---
## FieldAddressBlock::get_LanguageId method


Adresi biçimlendirmek için kullanılan dil kimliğini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_LanguageId()
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
