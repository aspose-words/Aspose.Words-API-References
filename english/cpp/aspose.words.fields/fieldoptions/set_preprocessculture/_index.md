---
title: Aspose::Words::Fields::FieldOptions::set_PreProcessCulture method
linktitle: set_PreProcessCulture
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::set_PreProcessCulture method. Sets the culture to preprocess field values in C++.'
type: docs
weight: 40000
url: /cpp/aspose.words.fields/fieldoptions/set_preprocessculture/
---
## FieldOptions::set_PreProcessCulture method


Sets the culture to preprocess field values.

```cpp
void Aspose::Words::Fields::FieldOptions::set_PreProcessCulture(const System::SharedPtr<System::Globalization::CultureInfo> & value)
```

## Remarks


Currently this property only affects value of the [FieldDocProperty](../../fielddocproperty/) field.

The default value is **null**. When this property is set to **null**, the [FieldDocProperty](../../fielddocproperty/) field's value is preprocessed with the culture controlled by the [FieldUpdateCultureSource](../get_fieldupdateculturesource/) property.
## Examples


Shows how to set the preprocess culture.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set the culture according to which some fields will format their displayed values.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// The DOCPROPERTY field will display its result formatted according to the preprocess culture
// we have set to German. The field will display the date/time using the "dd.mm.yyyy hh:mm" format.
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// After switching to the invariant culture, the DOCPROPERTY field will use the "mm/dd/yyyy hh:mm" format.
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```
## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
