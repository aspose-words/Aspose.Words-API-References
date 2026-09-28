---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress метод"
linktitle: "get_UserAddress"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress метод. Получает или задает почтовый адрес текущего пользователя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


Получает или задает почтовый адрес текущего пользователя.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## Примеры



Показывает, как использовать поле USERADDRESS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте объект UserInformation и установите его в качестве источника пользовательской информации для всех полей, которые мы создаём.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Создайте поле USERADDRESS, чтобы отобразить адрес текущего пользователя,
// полученное из объекта UserInformation, который мы создали выше.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// Мы можем установить это свойство, чтобы наше поле переопределило значение, текущо хранящееся в объекте UserInformation.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// Это не влияет на значение в объекте UserInformation.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## См. также

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
