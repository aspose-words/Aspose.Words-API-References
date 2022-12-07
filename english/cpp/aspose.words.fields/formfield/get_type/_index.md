---
title: get_Type
second_title: Aspose.Words for C++ API Reference
description: Returns the form field type.
type: docs
weight: 300
url: /cpp/aspose.words.fields/formfield/get_type/
---
## FormField::get_Type method


Returns the form field type.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FormField::get_Type()
```


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

* Enum [FieldType](../../fieldtype/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
