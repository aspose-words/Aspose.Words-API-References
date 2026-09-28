---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication метод"
linktitle: "get_NameOfApplication"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication метод. Получает или задает имя приложения в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_nameofapplication/
---
## BuiltInDocumentProperties::get_NameOfApplication method


Получает или задает имя приложения.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication()
```


## Примеры



Показывает, как работать со свойствами документа в категории "Origin".
```cpp
// Откройте документ, который мы создали и отредактировали с помощью Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Следующие встроенные свойства содержат информацию о создании и редактировании этого документа.
// Мы можем щелкнуть правой кнопкой мыши этот документ в Windows Explorer и найти
// эти свойства через "Properties" -> "Details" -> категорию "Origin".
// Поля, такие как PRINTDATE и EDITTIME, могут отображать эти значения в теле документа.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// Мы также можем изменить значения встроенных свойств.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word автоматически обновляет следующие свойства при сохранении документа.
// Чтобы использовать эти свойства с Aspose.Words, нам потребуется установить их значения вручную.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// Мы можем щелкнуть правой кнопкой мыши этот документ в Windows Explorer и найти эти свойства в "Properties" -> "Details" -> "Origin".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```

## См. также

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
