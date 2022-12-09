---
title: get_Name
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the form field name.
type: docs
weight: 183
url: /cpp/aspose.words.fields/formfield/get_name/
---
## FormField::get_Name method


Gets or sets the form field name.

```cpp
System::String Aspose::Words::Fields::FormField::get_Name()
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

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
