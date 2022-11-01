---
title: get_LanguageId
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the language ID used to format the address.
type: docs
weight: 53
url: /cpp/aspose.words.fields/fieldaddressblock/get_languageid/
---
## FieldAddressBlock.get_LanguageId method


Gets or sets the language ID used to format the address.

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_LanguageId()
```


## Examples




Shows how to insert an ADDRESSBLOCK field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto field = System::DynamicCast<FieldAddressBlock>(builder->InsertField(FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// Setting this to "2" will include all countries and regions,
// unless it is the one specified in the ExcludedCountryOrRegionName property.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// By default, this property will contain the language ID of the first character of the document.
// We can set a different culture for the field to format the result with like this.
field->set_LanguageId(System::Convert::ToString(MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(
    u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field->GetFieldCode());
```

