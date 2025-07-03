---
title: Aspose::Words::Fields::Field::get_LocaleId method
linktitle: get_LocaleId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::Field::get_LocaleId method. Gets or sets the LCID of the field in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


Gets or sets the LCID of the field.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## Examples



Shows how to insert a field and work with its locale. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a DATE field, and then print the date it will display.
// Your thread's current culture determines the formatting of the date.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// Changing the culture of our thread will impact the result of the DATE field.
// Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
// This way allows us to avoid changing the thread's culture to get this effect.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
