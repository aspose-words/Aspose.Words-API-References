---
title: "Aspose::Words::Fields::UserInformation فئة"
linktitle: "UserInformation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::UserInformation فئة. يحدد معلومات حول المستخدم. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 117000
url: /ar/cpp/aspose.words.fields/userinformation/
---
## UserInformation class


يحدد معلومات حول المستخدم. لمعرفة المزيد، زر مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class UserInformation : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Address](./get_address/)() const | يحصل أو يعيّن العنوان البريدي للمستخدم. |
| static [get_DefaultUser](./get_defaultuser/)() | معلومات المستخدم الافتراضية. |
| [get_Initials](./get_initials/)() const | يحصل أو يعيّن الأحرف الأولى للمستخدم. |
| [get_Name](./get_name/)() const | يحصل أو يعيّن اسم المستخدم. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Address](./set_address/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::UserInformation::get_Address](./get_address/). |
| [set_Initials](./set_initials/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::UserInformation::get_Initials](./get_initials/). |
| [set_Name](./set_name/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::UserInformation::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [UserInformation](./userinformation/)() |  |

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
