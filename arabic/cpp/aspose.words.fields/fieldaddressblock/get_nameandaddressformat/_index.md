---
title: "طريقة Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat"
linktitle: "get_NameAndAddressFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat. يحصل أو يضبط تنسيق الاسم والعنوان في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.fields/fieldaddressblock/get_nameandaddressformat/
---
## FieldAddressBlock::get_NameAndAddressFormat method


يحصل أو يعيّن تنسيق الاسم والعنوان.

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat()
```


## أمثلة



يوضح كيفية إدراج حقل ADDRESSBLOCK.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// ضبط هذا إلى "2" سيشمل جميع البلدان والمناطق،
// إلا إذا كان هو المحدد في خاصية ExcludedCountryOrRegionName.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// بشكل افتراضي، ستحتوي هذه الخاصية على معرف اللغة للحرف الأول في المستند.
// يمكننا تعيين ثقافة مختلفة للحقل لتنسيق النتيجة بهذه الطريقة.
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## انظر أيضًا

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
