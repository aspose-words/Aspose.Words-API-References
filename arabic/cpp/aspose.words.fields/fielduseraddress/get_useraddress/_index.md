---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress طريقة"
linktitle: "get_UserAddress"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress طريقة. يحصل على أو يحدد العنوان البريدي للمستخدم الحالي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


يحصل أو يعيّن عنوان البريد الحالي للمستخدم.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## أمثلة



يظهر كيفية استخدام حقل USERADDRESS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ كائن UserInformation وضعه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// أنشئ حقل USERADDRESS لعرض عنوان المستخدم الحالي،
// مستمد من كائن UserInformation الذي أنشأناه أعلاه.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// يمكننا تعيين هذه الخاصية لجعل حقلنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// هذا لا يؤثر على القيمة في كائن UserInformation.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## انظر أيضًا

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
