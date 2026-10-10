---
title: "Aspose::Words::Fields::UserInformation::get_DefaultUser طريقة"
linktitle: "get_DefaultUser"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::UserInformation::get_DefaultUser طريقة. معلومات المستخدم الافتراضية في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.fields/userinformation/get_defaultuser/
---
## UserInformation::get_DefaultUser method


معلومات المستخدم الافتراضية.

```cpp
static System::SharedPtr<Aspose::Words::Fields::UserInformation> Aspose::Words::Fields::UserInformation::get_DefaultUser()
```


## أمثلة



يعرض كيفية تعيين تفاصيل المستخدم وعرضها باستخدام الحقول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أنشئ كائن UserInformation واضبطه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// أدرج حقول USERNAME و USERINITIALS و USERADDRESS، التي تعرض قيم
// الخصائص المقابلة لكائن UserInformation الذي أنشأناه أعلاه.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// كائن خيارات الحقل يحتوي أيضًا على مستخدم افتراضي ثابت يمكن للحقول في جميع المستندات الإشارة إليه.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## انظر أيضًا

* Class [UserInformation](../)
* Class [UserInformation](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
