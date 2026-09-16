---
title: "Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat method"
linktitle: "get_NameAndAddressFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat 方法。获取或设置 C++ 中的姓名和地址格式。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fields/fieldaddressblock/get_nameandaddressformat/
---
## FieldAddressBlock::get_NameAndAddressFormat method


获取或设置名称和地址格式。

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat()
```


## 示例



展示如何插入 ADDRESSBLOCK 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// 将此设置为 "2" 将包含所有国家和地区，
// 除非它是 ExcludedCountryOrRegionName 属性中指定的那个。
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// 默认情况下，此属性将包含文档第一个字符的语言 ID。
// 我们可以为字段设置不同的区域性来格式化结果，如下所示。
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## 另见

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
