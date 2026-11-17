---
title: Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method
linktitle: get_LegacyNumberFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method. Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## Remarks


When this property is set to **true**, template symbol "#" worked as in .net: Replaces the pound sign with the corresponding digit if one is present; otherwise, no symbols appears in the result string.

When this property is set to **false**, template symbol "#" works as MS Word: This format item specifies the requisite numeric places to display in the result. If the result does not include a digit in that place, MS Word displays a space. For example, { = 9 + 6 \# $### } displays $ 15.

The default value is **false**.

## Examples



Shows how enable legacy number formatting for fields. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
