---
title: Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat method
linktitle: get_UseInvariantCultureNumberFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat method. Gets or sets the value indicating that number format is parsed using invariant culture or not in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


Gets or sets the value indicating that number format is parsed using invariant culture or not.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## Remarks


When this property is set to **true**, number format is taken from an invariant culture.

When this property is set to **false**, number format is taken from the current thread's culture.

The default value is **false**.

## Examples



Shows how to format numbers according to the invariant culture. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// Sometimes, fields may not format their numbers correctly under certain cultures.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// To fix this, we could change the culture for the entire thread.
// Another way to fix this is to set this flag,
// which gets all fields to use the invariant culture when formatting numbers.
// This way allows us to avoid changing the culture for the entire thread.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
