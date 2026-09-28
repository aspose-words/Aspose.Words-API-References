---
title: "метод Aspose::Words::Fields::FieldUserInitials::get_UserInitials"
linktitle: "get_UserInitials"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Fields::FieldUserInitials::get_UserInitials. Получает или задает инициалы текущего пользователя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


Получает или задаёт инициалы текущего пользователя.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## Примеры



Показывает, как использовать поле USERINITIALS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте объект UserInformation и установите его в качестве источника пользовательской информации для всех полей, которые мы создаём.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Создайте поле USERINITIALS для отображения инициалов текущего пользователя,
// полученное из объекта UserInformation, который мы создали выше.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// Мы можем установить это свойство, чтобы наше поле переопределило значение, текущо хранящееся в объекте UserInformation.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// Это не влияет на значение в объекте UserInformation.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## См. также

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
