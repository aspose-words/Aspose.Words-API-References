---
title: get_Result
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a string that represents the result of this form field.
type: docs
weight: 222
url: /cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


Gets or sets a string that represents the result of this form field.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## Remarks


For a text form field the result is the text that is in the field.

For a checkbox form field the result can be "1" or "0" to indicate checked or unchecked.

For a dropdown form field the result is the string selected in the dropdown.

Setting [Result](./) for a text form field does not apply the text format specified in [TextInputFormat](../get_textinputformat/). If you want to set a value and apply the format, use the [SetTextInputValue()](../) method.

For a text form field the [TextInputDefault](../get_textinputdefault/) value is applied if value is **null**.

## Examples



Shows how to insert a combo box. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Insert a combo box which will allow a user to choose an option from a collection of strings.
SharedPtr<FormField> comboBox = builder->InsertComboBox(u"MyComboBox", MakeArray<String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// The form field will appear in the form of a "select" html tag.
doc->Save(ArtifactsDir + u"FormFields.Create.html");
```

## See Also

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
