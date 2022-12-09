---
title: get_LocaleId
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the LCID of the field.
type: docs
weight: 105
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a DATE field, and then print the date it will display.
// Your thread's current culture determines the formatting of the date.
SharedPtr<Field> field = builder->InsertField(u"DATE");
std::cout << "Today's date, as displayed in the \"" << System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName()
          << "\" culture: " << field->get_Result() << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// Changing the culture of our thread will impact the result of the DATE field.
// Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
// This way allows us to avoid changing the thread's culture to get this effect.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(FieldUpdateCultureSource::FieldCode);
auto de = MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << "Today's date, as displayed according to the \""
          << System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName() << "\" culture: " << field->get_Result()
          << std::endl;
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
