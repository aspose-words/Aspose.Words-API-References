---
title: "Aspose::Words::Fields::Field::get_LocaleId method"
linktitle: "get_LocaleId"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::Field::get_LocaleId method. Hämtar eller anger fältets LCID i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


Hämtar eller anger LCID för fältet.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## Exempel



Visar hur man infogar ett fält och arbetar med dess språk.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett DATE-fält och skriv sedan ut datumet som det kommer att visa.
// Trådens aktuella kultur bestämmer datumformatet.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// Att ändra trådens kultur kommer att påverka resultatet av DATE-fältet.
// Ett annat sätt att få DATE-fältet att visa ett datum i en annan kultur är att använda dess LocaleId-egenskap.
// Detta sätt låter oss undvika att ändra trådens kultur för att uppnå denna effekt.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## Se även

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
