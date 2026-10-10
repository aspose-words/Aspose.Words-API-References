---
title: "طريقة Aspose::Words::Fields::FormField::get_Name"
linktitle: "get_Name"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FormField::get_Name. يحصل على اسم حقل النموذج أو يضبطه في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.fields/formfield/get_name/
---
## FormField::get_Name method


يحصل على أو يضبط اسم حقل النموذج.

```cpp
System::String Aspose::Words::Fields::FormField::get_Name()
```


## أمثلة



يوضح كيفية إدراج مربع اختيار.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// أدرج مربع اختيار يتيح للمستخدم اختيار خيار من مجموعة من السلاسل.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// سيظهر حقل النموذج على شكل وسم HTML "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## انظر أيضًا

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
