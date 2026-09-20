---
title: "Aspose::Words::Fields::UserInformation класс"
linktitle: "UserInformation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::UserInformation класс. Указывает информацию о пользователе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 117000
url: /ru/cpp/aspose.words.fields/userinformation/
---
## UserInformation class


Указывает информацию о пользователе. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class UserInformation : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Address](./get_address/)() const | Получает или задаёт почтовый адрес пользователя. |
| static [get_DefaultUser](./get_defaultuser/)() | Информация пользователя по умолчанию. |
| [get_Initials](./get_initials/)() const | Получает или задаёт инициалы пользователя. |
| [get_Name](./get_name/)() const | Получает или задаёт имя пользователя. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Address](./set_address/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::UserInformation::get_Address](./get_address/). |
| [set_Initials](./set_initials/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::UserInformation::get_Initials](./get_initials/). |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::UserInformation::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [UserInformation](./userinformation/)() |  |

## Примеры



Показывает, как задать детали пользователя и отобразить их с помощью полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте объект UserInformation и установите его в качестве источника данных для полей, отображающих информацию о пользователе.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Вставьте поля USERNAME, USERINITIALS и USERADDRESS, которые отображают значения
// соответствующих свойств объекта UserInformation, который мы создали выше.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// Объект параметров полей также имеет статического пользователя по умолчанию, к которому могут обращаться поля из всех документов.
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

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
