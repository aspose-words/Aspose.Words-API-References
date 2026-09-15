---
title: "طريقة Aspose::Words::Fields::FieldUserInitials::get_UserInitials"
linktitle: "get_UserInitials"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldUserInitials::get_UserInitials. يحصل على أو يحدد الأحرف الأولى للمستخدم الحالي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


يحصل أو يضبط الأحرف الأولى للمستخدم الحالي.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## أمثلة



يوضح كيفية استخدام حقل USERINITIALS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ كائن UserInformation وضعه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// أنشئ حقل USERINITIALS لعرض الأحرف الأولى للمستخدم الحالي،
// مستمد من كائن UserInformation الذي أنشأناه أعلاه.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// يمكننا تعيين هذه الخاصية لجعل حقلنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// هذا لا يؤثر على القيمة في كائن UserInformation.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## انظر أيضًا

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
