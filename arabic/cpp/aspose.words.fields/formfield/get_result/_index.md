---
title: "Aspose::Words::Fields::FormField::get_Result طريقة."
linktitle: "get_Result"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FormField::get_Result طريقة. يحصل على أو يعيّن سلسلة تمثل نتيجة هذا الحقل في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


يحصل على أو يضبط سلسلة تمثل نتيجة هذا الحقل النموذج.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## ملاحظات


بالنسبة لحقل نموذج نصي، النتيجة هي النص الموجود في الحقل.

بالنسبة لحقل نموذج مربع اختيار، يمكن أن تكون النتيجة \"1\" أو \"0\" للدلالة على تحديد أو عدم التحديد.

بالنسبة لحقل نموذج قائمة منسدلة، النتيجة هي السلسلة المختارة في القائمة المنسدلة.

تعيين [Result](./) لحقل نموذج نصي لا يطبق تنسيق النص المحدد في [TextInputFormat](../get_textinputformat/). إذا كنت تريد تعيين قيمة وتطبيق التنسيق، استخدم طريقة [SetTextInputValue()](../).

بالنسبة لحقل نموذج نصي، يتم تطبيق قيمة [TextInputDefault](../get_textinputdefault/) إذا كان *value* **null**.

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
