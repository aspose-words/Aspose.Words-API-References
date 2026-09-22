---
title: "طريقة Aspose::Words::Fields::FieldUserName::get_UserName"
linktitle: "get_UserName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldUserName::get_UserName. تسترجع أو تضبط اسم المستخدم الحالي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


يحصل أو يعيّن اسم المستخدم الحالي.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## أمثلة



يظهر كيفية استخدام حقل USERNAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ كائن UserInformation وضعه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أنشئ حقل USERNAME لعرض اسم المستخدم الحالي،
// مستمد من كائن UserInformation الذي أنشأناه أعلاه.
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// يمكننا تعيين هذه الخاصية لجعل حقلنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// هذا لا يؤثر على القيمة في كائن UserInformation.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## انظر أيضًا

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
