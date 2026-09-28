---
title: "Класс Aspose::Words::Properties::DocumentPropertyCollection"
linktitle: "DocumentPropertyCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Properties::DocumentPropertyCollection. Базовый класс для коллекций BuiltInDocumentProperties и CustomDocumentProperties. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class


Базовый класс для коллекций [BuiltInDocumentProperties](../builtindocumentproperties/) и [CustomDocumentProperties](../customdocumentproperties/). Чтобы узнать больше, посетите статью документации [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clear](./clear/)() | Удаляет все свойства из коллекции. |
| [Contains](./contains/)(const System::String\&) | Возвращает **true**, если в коллекции существует свойство с указанным именем. |
| [get_Count](./get_count/)() | Получает количество элементов в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех элементов в коллекции. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](./idx_get/)(System::String) | Возвращает объект [DocumentProperty](../documentproperty/) по имени свойства. |
| [idx_get](./idx_get/)(int32_t) | Возвращает объект [DocumentProperty](../documentproperty/) по индексу. |
| [IndexOf](./indexof/)(const System::String\&) | Получает индекс свойства по имени. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Удаляет из коллекции свойство с указанным именем. |
| [RemoveAt](./removeat/)(int32_t) | Удаляет свойство по указанному индексу. |
| static [Type](./type/)() |  |
## Примечания


Имена свойств не чувствительны к регистру.

Свойства в коллекции сортируются в алфавитном порядке по имени.

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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
