---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber метод"
linktitle: "get_RevisionNumber"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber метод. Получает или задаёт номер ревизии документа в C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_revisionnumber/
---
## BuiltInDocumentProperties::get_RevisionNumber method


Получает или задает номер ревизии документа.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber()
```

## Примечания


Aspose.Words не обновляет это свойство.

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


Показывает, как работать с полями REVNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Current revision #");

// Вставьте поле REVNUM, которое отображает свойство текущего номера ревизии документа.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRevNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRevisionNum, true));

ASSERT_EQ(u" REVNUM ", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_RevisionNumber());

// Это свойство считает, сколько раз документ был сохранён в Microsoft Word,
// и не связано с отслеживаемыми изменениями. Мы можем найти его, щёлкнув правой кнопкой мыши по документу в Проводнике Windows
// через Свойства -> Подробности. Мы можем обновить это свойство вручную.
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LVAL_LAMBDA_ARGS(doc->get_BuiltInDocumentProperties(), RevisionNumber));
field->Update();

ASSERT_EQ(u"2", field->get_Result());
```

## См. также

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
