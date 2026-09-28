---
title: "Aspose::Words::Properties::DocumentPropertyCollection::Contains метод"
linktitle: "Contains"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentPropertyCollection::Contains метод. Возвращает true, если свойство с указанным именем существует в коллекции в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.properties/documentpropertycollection/contains/
---
## DocumentPropertyCollection::Contains method


Возвращает **true**, если в коллекции существует свойство с указанным именем.

```cpp
bool Aspose::Words::Properties::DocumentPropertyCollection::Contains(const System::String &name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя свойства без учёта регистра. |

### ReturnValue

**true** if the property exists in the collection; **false** otherwise.

## Примеры



Показывает, как работать с пользовательскими свойствами документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Пользовательские свойства документа представляют собой пары ключ‑значение, которые мы можем добавить в документ.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Коллекция сортирует пользовательские свойства в алфавитном порядке.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Выведите каждое пользовательское свойство в документе.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Отобразите значение пользовательского свойства с помощью поля DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Мы можем найти эти пользовательские свойства в Microsoft Word через "File" -> "Properties" > "Advanced Properties" > "Custom".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Ниже представлены три способа удаления пользовательских свойств из документа.
// 1 -  Удалить по индексу:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Удалить по имени:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Очистить всю коллекцию сразу:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## См. также

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
