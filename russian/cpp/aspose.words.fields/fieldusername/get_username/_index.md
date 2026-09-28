---
title: "Метод Aspose::Words::Fields::FieldUserName::get_UserName"
linktitle: "get_UserName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldUserName::get_UserName. Получает или задает имя текущего пользователя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


Получает или задает имя текущего пользователя.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## Примеры



Показывает, как использовать поле USERNAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте объект UserInformation и установите его в качестве источника пользовательской информации для всех полей, которые мы создаём.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле USERNAME, чтобы отобразить имя текущего пользователя,
// полученное из объекта UserInformation, который мы создали выше.
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// Мы можем установить это свойство, чтобы наше поле переопределило значение, текущо хранящееся в объекте UserInformation.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// Это не влияет на значение в объекте UserInformation.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## См. также

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
