---
title: "Метод Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName"
linktitle: "get_ExcludedCountryOrRegionName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName method. Получает или задает название исключённой страны/региона в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldaddressblock/get_excludedcountryorregionname/
---
## FieldAddressBlock::get_ExcludedCountryOrRegionName method


Получает или задает название исключённой страны/региона.

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName()
```


## Примеры



Показывает, как вставить поле ADDRESSBLOCK.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// Установка этого значения в "2" включит все страны и регионы,
// если только это не указано в свойстве ExcludedCountryOrRegionName.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// По умолчанию это свойство будет содержать идентификатор языка первого символа документа.
// Мы можем установить другую культуру для поля, чтобы отформатировать результат, например, так.
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## См. также

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
