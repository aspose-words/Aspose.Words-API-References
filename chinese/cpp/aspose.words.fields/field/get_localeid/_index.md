---
title: "Aspose::Words::Fields::Field::get_LocaleId 方法"
linktitle: "get_LocaleId"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::Field::get_LocaleId 方法。获取或设置字段的 LCID（在 C++ 中）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


获取或设置字段的 LCID。

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## 示例



展示如何插入字段并使用其区域设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个 DATE 字段，然后打印它将显示的日期。
// 线程的当前区域性决定日期的格式。
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// 更改线程的区域性会影响 DATE 字段的结果。
// 让 DATE 字段在不同区域性下显示日期的另一种方法是使用其 LocaleId 属性。
// 这种方式使我们无需更改线程的区域性即可实现此效果。
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## 另见

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
